# script b75769dbdeab4a399cddb5bd9db3d85f

* **helm**
  * in this use case is just a templating engine. Since there are many microservices and only some values are different. you can use a template yaml file and pass a range of values into it

```text
#!/bin/bash

set -e
set -o pipefail

LINE_BREAK='*************************************************************'
trap 'echo -e "$LINE_BREAK\\nFAILED\\n$LINE_BREAK"' ERR

WAYPOINT_VERSION=vdod-202003051700
ALVA_HELM_CHART_VERSION=0.2.0-20201130T132448Z-125de01
FED_STACK=us-gov-1
SERVICES=()
TENANTS=()
DEPLOY_CORE=true
VERBOSE=false
DRY_RUN=false

while getopts ":vdhw:a:r:s:t:e:c:" opt; do
  case ${opt} in
    w )
      WAYPOINT_VERSION=$OPTARG
      ;;
    a )
      ALVA_HELM_CHART_VERSION=$OPTARG
      ;;
    r )
      FED_REGION=$OPTARG
      ;;
    e )
      ENCRYPTION_KEY_LOCATION=$OPTARG
      ;;
    s )
      SERVICES+=("$OPTARG")
      ;;
    t )
      TENANTS+=("$OPTARG")
      ;;
    c )
      DEPLOY_CORE="$OPTARG"
      ;;
    d )
      DRY_RUN=true
      ;;
    v )
      VERBOSE=true
      ;;
    h )
      echo "Usage fed_deploy.sh  -r <region> -e <key_location>"
      echo "Options:"
      echo "  -r <region>: Federal Region (cluster name) to deploy, e.g. vsphere-kc-k8s-hacas-mid-0, required"
      echo "  -e <key_location>: The file location containing the Alva encryption key, used for secret upload,"
      echo "         required if not a DRY_RUN (-d)"
      echo "  -c <true/false>: Determine if the core services (edge, mlconfig, eureka, watt) should be deployed,"
      echo "         defaults to true"
      echo "  -t <tenant>: The tenant (in norbert form, e.g. b1930-lcahncrls-net) to deploy, can be repeated for"
      echo "         multiple tenants. If not supplied all tenants will be deployed"
      echo "  -s <service_name>: The consumer service (in norbert form, e.g. mlallergy) to deploy, can be repeated for"
      echo "         multiple services. If not supplied all services will be deployed"
      echo "  -a <helm_version>: The Alva helm chart version, defauts to $ALVA_HELM_CHART_VERSION"
      echo "  -w <waypoint_version>: The waypoint version to use to generate config and upload secrets, defaults to $WAYPOINT_VERSION"
      echo "  -d: Indicates this is a DRY_RUN, if set the script will skip applying any changes, used to allow local testing"
      echo "  -v: Verbose mode, will output additional messages to assist with troubleshooting"
      exit 0
      ;;
    : )
      echo "Option [$OPTARG] requires an argument"
      exit 1
      ;;
    ? )
      echo "Uknown option [$OPTARG] provided"
      exit 1
      ;;
  esac
done
shift $((OPTIND -1))

if [ ${#TENANTS[@]} -eq 0 ]; then
  TENANTS=(
  b1930-lcahncrls-net
  i1930-lcahncrls-net
  b0630-lcahncrls-net
  c0630-lcahncrls-net
  m0630-lcahncrls-net
  p0630-lcahncrkc-net
  )
fi

if [ -z "$FED_REGION" ]; then
  echo "FED_REGION option [-r] must be provided"
  exit 1
fi

# Using grep here both as a quick parser and to read in input
# shellcheck disable=SC2207
EUREKA_AZS=( $(grep -A 10 "$FED_REGION" ./production_fed/norbert_config.yaml | grep -A 3 'eureka_azs' | tail -n 3 | sed 's/^\( *- \)//') )

if [ "$DRY_RUN" = false ]; then
  if [ -z "$ENCRYPTION_KEY_LOCATION" ]; then
    echo "ENCRYPTION_KEY_LOCATION option [-e] must be provided"
    exit 1
  elif ! [ -r "$ENCRYPTION_KEY_LOCATION" ]; then
    echo "Provided ENCRYPTION_KEY_LOCATION [$ENCRYPTION_KEY_LOCATION] does not exist or is not readable"
    exit 1
  else
    # Assigning the contents of the key to an variable because file permissions/ownership are touchy in the federal space
    # shellcheck disable=SC2034
    ENCRYPTION_KEY=$(cat "$ENCRYPTION_KEY_LOCATION")
  fi
fi

if [ "$VERBOSE" = true ]; then
  echo "Options:"
  echo "  FED_REGION (-r) [$FED_REGION]"
  echo "  ENCRYPTION_KEY_LOCATION (-e) [$ENCRYPTION_KEY_LOCATION]"
  echo "  WAYPOINT_VERSION (-w) [$WAYPOINT_VERSION]"
  echo "  ALVA_HELM_CHART_VERSION (-a) [$ALVA_HELM_CHART_VERSION]"
  echo "  DEPLOY_CORE (-c) [$DEPLOY_CORE]"
  echo "  DRY_RUN (-d) [$DRY_RUN]"
  echo "  VERBOSE (-v) [$VERBOSE]"
  echo "  SERVICES:"
  if [ ${#SERVICES[@]} -eq 0 ]; then
    echo "    All"
  else
    printf '    %s\n' "${SERVICES[@]}"
  fi
  echo "  TENANTS:"
  printf '    %s\n' "${TENANTS[@]}"
  echo "  EUREKA_AZS:"
  printf '    %s\n' "${EUREKA_AZS[@]}"
fi

# These are both templates that we don't want to expand in their current form
# shellcheck disable=SC2016
UPLOAD_SECRETS_CMD_TEMPLATE='docker run --rm
  -v "${PWD}"/output:/output -v "${PWD}"/config:/config -v "${PWD}/norbert-config":/usr/config
  -e WAYPOINT_CONFIG_LOCATION=/config
  docker-production.cernerrepos.net/norbert/waypoint:$WAYPOINT_VERSION
  upload-secrets
  --secret-encryption-key "$ENCRYPTION_KEY"
  -p "alva"
  -a "$2"
  -s "$FED_STACK"
  -r "$FED_REGION"'

if [ "$VERBOSE" = true ]; then
  UPLOAD_SECRETS_CMD_TEMPLATE+=' --trace'
fi

# shellcheck disable=SC2016
GENERATE_CONFIG_CMD_TEMPLATE='docker run --rm
  -v "${PWD}"/output:/output -v "${PWD}"/config:/config -v "${PWD}/norbert-config":/usr/config
  -e WAYPOINT_CONFIG_LOCATION=/config
  docker-production.cernerrepos.net/norbert/waypoint:$WAYPOINT_VERSION
  generate-config
  --output-dir /output
  -p "alva"
  -a "$2"
  -s "$FED_STACK"
  -r "$FED_REGION"'

if [ "$VERBOSE" = true ]; then
  GENERATE_CONFIG_CMD_TEMPLATE+=' --trace'
fi

# Simple bash function which takes an application name as the first argument
# and an optional tenant name as the 2nd and will:
# 1. Invoke waypoint to upload secrets
# 2. Invoke Waypoint to generate config
# 3. Apply the generated config to the alva-service HELM template
# 4. Invoke kubectl apply on the generated manifest
deploy_application() {
  NAME=$1
  if [[ -n "$2" ]]
  then
    NAME+="-$2"
  fi
  upload_secrets "$NAME" "$1" "$2"
  generate_config "$NAME" "$1" "$2"
  apply_helm_template "$NAME" "$1" "$2"
  echo "Deploying Manifest - $NAME"
  if [ "$DRY_RUN" = false ]; then
    kubectl --namespace=alva-prod --kubeconfig='./output/kubeconfig.yaml' apply -f "./output/$NAME.yaml"
  fi
}

upload_secrets() {
  echo "Uploading Secrets - $1"
  UPLOAD_SECRETS_CMD=$UPLOAD_SECRETS_CMD_TEMPLATE
  # If there is a tenant add the -n flag to the command
  if [[ -n "$3" ]]
  then
    UPLOAD_SECRETS_CMD+=" -n $3"
  fi
  if [ "$DRY_RUN" = false ]; then
    # shellcheck disable=SC2086
    eval $UPLOAD_SECRETS_CMD
  fi
}

generate_config() {
  echo "Generating Config - $1"
  GENERATE_CONFIG_CMD=$GENERATE_CONFIG_CMD_TEMPLATE
  # If there is a tenant add the -n flag to the command
  if [[ -n "$3" ]]
  then
    GENERATE_CONFIG_CMD+=" -n $3"
  fi

  # shellcheck disable=SC2086
  eval $GENERATE_CONFIG_CMD
}

apply_helm_template() {
  # For whatever reason the fed environment is somewhat finicky, as such using cat to pass | input to jq.
  # shellcheck disable=SC2002
  DOCKER_IMAGE=$(cat profiles/alva/"$2".yml | grep -m 1 'image' | sed 's/image\: \(.*\)$/\1/' | tr -d '[:space:]')
  echo "Applying Helm template - $1"
  helm --set project=alva \
     --set application="$2" \
     --set dockerImage="$DOCKER_IMAGE" \
     --set dockerRepository=alva \
     --set region="$FED_REGION" \
     --set stack="$FED_STACK" \
     --set tenant="$3" \
     --values ./output/config.json template ./alva-service > "./output/$1.yaml"
}

echo "Creating Working Directory"
cd "$HOME"
# We only want the first element since we're using that as a quick and dirty seed name that still provides some
# minimum context around which directory this job is tied too
# shellcheck disable=SC2128
DIR_NAME=alva_tmp_$(echo "$TENANTS" | cut -d'-' -f 1)
mkdir "$DIR_NAME"
cd "$DIR_NAME"

echo "Cloning norbert-config"
git clone https://github.cerner.com/norbert/norbert-config
cd norbert-config
git clone https://github.cerner.com/norbert/norbert-config
chmod -R 777 norbert-config

wget "https://cernerrepos.net:443/helm-production/alva/alva-service-$ALVA_HELM_CHART_VERSION.tgz"
tar -xvf "alva-service-$ALVA_HELM_CHART_VERSION.tgz"
# For DRY_RUN don't chown as that breaks local testing
if [ "$DRY_RUN" = false ]; then
  chown -R 100:101 ./alva-service
else
  chmod -R 777 ./alva-service
fi

echo "Creating waypoint.yaml"
cat > ./config/waypoint.yaml <<- EOF
---
providers:
  kube:
    enabled: true
    secretSynchronization:
      # This is to control whether a provider should have secret synchronization
      enabled: true
    clusters:
      $FED_REGION:
        environment: prod
        configFile: /output/kubeconfig.yaml
        certManager:
          enabled: true
          defaultSelfSigningIssuer: default-self-signing-issuer
EOF

if [ "$DRY_RUN" = false ]; then
  chown -R 100:101 ./config
else
  chmod -R 777 ./config
fi

echo "Initializing kubectl context"
mkdir ./output
if [ "$DRY_RUN" =  false ]; then
  cp "/root/.kube/$FED_REGION/config" ./output/kubeconfig.yaml
  chown -R 100:101 ./output
else
  chmod -R 777 ./output
fi

if [ "$DEPLOY_CORE" = true ]; then
  for EUREKA_AZ in ${EUREKA_AZS[*]}
  do
    deploy_application  "eureka" "$EUREKA_AZ"
    echo "Waiting for eureka-$EUREKA_AZ to report Ready"
    if [ "$DRY_RUN" = false ]; then
      kubectl --namespace=alva-prod --kubeconfig='./output/kubeconfig.yaml' wait --timeout=310s --for=condition=Ready pod -l "norbert.cerner.com/tenant=$EUREKA_AZ,norbert.cerner.com/application=eureka"
    fi
  done

  deploy_application 'edge'
  echo "Waiting for edge to report Ready"
  if [ "$DRY_RUN" = false ]; then
    kubectl --namespace=alva-prod --kubeconfig='./output/kubeconfig.yaml' wait --timeout=130s --for=condition=Ready pod -l norbert.cerner.com/application=edge
  fi
  deploy_application 'watt'
  echo "Waiting for watt to report Ready"
  if [ "$DRY_RUN" = false ]; then
    kubectl --namespace=alva-prod --kubeconfig='./output/kubeconfig.yaml' wait --timeout=130s --for=condition=Ready pod -l norbert.cerner.com/application=watt
  fi

  deploy_application 'mlconfig'
  echo "Waiting for mlconfig to report Ready"
  if [ "$DRY_RUN" = false ]; then
    kubectl --namespace=alva-prod --kubeconfig='./output/kubeconfig.yaml' wait --timeout=130s --for=condition=Ready pod -l norbert.cerner.com/application=mlconfig
  fi
elif [ "$VERBOSE" = true ]; then
  echo "Skipping core services"
fi

if [ ${#SERVICES[@]} -eq 0 ]; then
  # False positive, returned value is also an array
  # shellcheck disable=SC2178
  SERVICES=$(find ./config/alva/app -name 'us-gov-1' | grep ml | grep -v mlconfig | sed 's|./config/alva/app/\([a-z]*\)/us-gov-1|\1|g')
fi

if [ "$VERBOSE" = true ]; then
  echo "Final Service List"
  printf '  %s\n' "${SERVICES[@]}"
fi

for TENANT in ${TENANTS[*]}
do
  for SERVICE in ${SERVICES[*]}
  do
    if [ -r "./config/alva/app/$SERVICE/$FED_STACK/$FED_REGION/$TENANT.yml.erb" ]; then
      deploy_application "$SERVICE" "$TENANT"
    elif [ "$VERBOSE" = true ]; then
      echo "Service [$SERVICE] is not deployed for tenant [$TENANT], skipping"
    fi
  done
  echo "Waiting for Consumer services in $TENANT to report Ready"
  if [ "$DRY_RUN" = false ]; then
    kubectl --namespace=alva-prod --kubeconfig='./output/kubeconfig.yaml' wait --timeout=300s --for=condition=Ready pod -l norbert.cerner.com/tenant="$TENANT"
  fi
done

cd "$HOME"
echo "Removing $HOME/$DIR_NAME"
rm -rf "${HOME:?}/${DIR_NAME:?}"

echo -e "$LINE_BREAK\\nSUCCESS!\\n$LINE_BREAK"
```

