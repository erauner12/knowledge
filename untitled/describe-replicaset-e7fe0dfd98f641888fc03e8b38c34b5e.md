# describe ReplicaSet e7fe0dfd98f641888fc03e8b38c34b5e

```bash
✘ er046256@w1738944  ~/tmp/Container-Masterclass-Codes/CC_Kubernetes/S12  kubectl describe rs mlworkflowevents-staging-stgeng-temp-rho-cernerasp-com-9975d9fd9
Name:           mlworkflowevents-staging-stgeng-temp-rho-cernerasp-com-9975d9fd9
Namespace:      alva-prod
Selector:       norbert.cerner.com/application=mlworkflowevents,norbert.cerner.com/project=alva,norbert.cerner.com/region=open-kc-k8s-asp-mid-0,norbert.cerner.com/stack=staging,norbert.cerner.com/tenant=stgeng-temp-rho-cernerasp-com,pod-template-hash=9975d9fd9
Labels:         app.kubernetes.io/managed-by=spinnaker
                app.kubernetes.io/name=mlworkflowevents
                norbert.cerner.com/application=mlworkflowevents
                norbert.cerner.com/consume-alva-eureka-staging-us-asp-kc-8a-main=true
                norbert.cerner.com/consume-alva-eureka-staging-us-asp-kc-8b-main=true
                norbert.cerner.com/consume-alva-eureka-staging-us-asp-kc-8c-main=true
                norbert.cerner.com/consume-alva-mlconfig-staging-main=true
                norbert.cerner.com/consume-alva-mlwebtoken-staging-stgeng-temp-rhoc3e6cfddf093b6ac=true
                norbert.cerner.com/exposeTo-alva-edge-staging=true
                norbert.cerner.com/exposeTo-alva-watt-staging=true
                norbert.cerner.com/external-149.45.12.15=true
                norbert.cerner.com/external-170.71.223.166=true
                norbert.cerner.com/external-antivirus-service.sandboxcernerpowerchart.net=true
                norbert.cerner.com/external-antivirus-service.stagingcernerpowerchart.com=true
                norbert.cerner.com/external-assignment-api.cloud-staging.sandboxcareaware.net=true
                norbert.cerner.com/external-ipolyldap01.northamerica.cerner.net=true
                norbert.cerner.com/external-ipsolgmibus01.ip.devcerner.net=true
                norbert.cerner.com/external-mill-alva-test.api.staginghealtheintent.com=true
                norbert.cerner.com/external-new-relic=true
                norbert.cerner.com/external-pod002-distcache-test-ls-cachenode-001.cernerasp.com=true
                norbert.cerner.com/external-pod002-distcache-test-ls-cachenode-002.cernerasp.com=true
                norbert.cerner.com/external-pod002-distcache-test-ls-cachenode-003.cernerasp.com=true
                norbert.cerner.com/external-staging-base-network=true
                norbert.cerner.com/external-tmprhoctx67.cmsext.com=true
                norbert.cerner.com/helm=0.2.0-20201201T133842Z-1ccc6f1
                norbert.cerner.com/profile=alva-mlworkflowevents-staging-stgeng-temp-rho-cernerasp-com
                norbert.cerner.com/project=alva
                norbert.cerner.com/region=open-kc-k8s-asp-mid-0
                norbert.cerner.com/stack=staging
                norbert.cerner.com/tenant=stgeng-temp-rho-cernerasp-com
                pod-template-hash=9975d9fd9
Annotations:    artifact.spinnaker.io/location: alva-prod
                artifact.spinnaker.io/name: mlworkflowevents-staging-stgeng-temp-rho-cernerasp-com
                artifact.spinnaker.io/type: kubernetes/deployment
                deployment.kubernetes.io/desired-replicas: 2
                deployment.kubernetes.io/max-replicas: 3
                deployment.kubernetes.io/revision: 18
                deployment.kubernetes.io/revision-history: 16
                moniker.spinnaker.io/application: mlworkflowevents
                moniker.spinnaker.io/cluster: mlworkflowevents-staging-stgeng-temp-rho-cernerasp-com
                moniker.spinnaker.io/detail: -stgeng-temp-rho-cernerasp-com
                moniker.spinnaker.io/stack: staging
                norbert.cerner.com/MCS_POINTS_OF_CONTACT:
                  Srinivasa.Ramasamy@cerner.com,Abhinav.Anishetti@cerner.com,Sagar.Burra@cerner.com,Sardar.Mohammed@cerner.com
                norbert.cerner.com/MCS_application: mlworkflowevents
                norbert.cerner.com/MCS_project: alva
                norbert.cerner.com/MCS_region: open-kc-k8s-asp-mid-0
                norbert.cerner.com/MCS_stack: staging
                norbert.cerner.com/MCS_tenant: stgeng-temp-rho-cernerasp-com
                norbert.cerner.com/com.cerner.repo_sha: 9e89d26c529bb23ccb948930ca6c0a359f039979
                norbert.cerner.com/com.cerner.repo_url:
                  https://raw.github.cerner.com/alva/alva-config/add5f517015b2f995970883eab96de2eb2c9880d/docs/ml-workflow-events.yaml
                norbert.cerner.com/splunk-index: alva
                norbert.cerner.com/splunk-source: docker-integration.cernerrepos.net/alva/ml-workflow-events:1.5-20201211T204430Z
Controlled By:  Deployment/mlworkflowevents-staging-stgeng-temp-rho-cernerasp-com
Replicas:       0 current / 0 desired
Pods Status:    0 Running / 0 Waiting / 0 Succeeded / 0 Failed
Pod Template:
  Labels:       app.kubernetes.io/managed-by=spinnaker
                app.kubernetes.io/name=mlworkflowevents
                norbert.cerner.com/application=mlworkflowevents
                norbert.cerner.com/consume-alva-eureka-staging-us-asp-kc-8a-main=true
                norbert.cerner.com/consume-alva-eureka-staging-us-asp-kc-8b-main=true
                norbert.cerner.com/consume-alva-eureka-staging-us-asp-kc-8c-main=true
                norbert.cerner.com/consume-alva-mlconfig-staging-main=true
                norbert.cerner.com/consume-alva-mlwebtoken-staging-stgeng-temp-rhoc3e6cfddf093b6ac=true
                norbert.cerner.com/exposeTo-alva-edge-staging=true
                norbert.cerner.com/exposeTo-alva-watt-staging=true
                norbert.cerner.com/external-149.45.12.15=true
                norbert.cerner.com/external-170.71.223.166=true
                norbert.cerner.com/external-antivirus-service.sandboxcernerpowerchart.net=true
                norbert.cerner.com/external-antivirus-service.stagingcernerpowerchart.com=true
                norbert.cerner.com/external-assignment-api.cloud-staging.sandboxcareaware.net=true
                norbert.cerner.com/external-ipolyldap01.northamerica.cerner.net=true
                norbert.cerner.com/external-ipsolgmibus01.ip.devcerner.net=true
                norbert.cerner.com/external-mill-alva-test.api.staginghealtheintent.com=true
                norbert.cerner.com/external-new-relic=true
                norbert.cerner.com/external-pod002-distcache-test-ls-cachenode-001.cernerasp.com=true
                norbert.cerner.com/external-pod002-distcache-test-ls-cachenode-002.cernerasp.com=true
                norbert.cerner.com/external-pod002-distcache-test-ls-cachenode-003.cernerasp.com=true
                norbert.cerner.com/external-staging-base-network=true
                norbert.cerner.com/external-tmprhoctx67.cmsext.com=true
                norbert.cerner.com/helm=0.2.0-20201201T133842Z-1ccc6f1
                norbert.cerner.com/profile=alva-mlworkflowevents-staging-stgeng-temp-rho-cernerasp-com
                norbert.cerner.com/project=alva
                norbert.cerner.com/region=open-kc-k8s-asp-mid-0
                norbert.cerner.com/stack=staging
                norbert.cerner.com/tenant=stgeng-temp-rho-cernerasp-com
                pod-template-hash=9975d9fd9
  Annotations:  artifact.spinnaker.io/location: alva-prod
                artifact.spinnaker.io/name: mlworkflowevents-staging-stgeng-temp-rho-cernerasp-com
                artifact.spinnaker.io/type: kubernetes/deployment
                moniker.spinnaker.io/application: mlworkflowevents
                moniker.spinnaker.io/cluster: mlworkflowevents-staging-stgeng-temp-rho-cernerasp-com
                moniker.spinnaker.io/detail: -stgeng-temp-rho-cernerasp-com
                moniker.spinnaker.io/stack: staging
                norbert.cerner.com/MCS_POINTS_OF_CONTACT:
                  Srinivasa.Ramasamy@cerner.com,Abhinav.Anishetti@cerner.com,Sagar.Burra@cerner.com,Sardar.Mohammed@cerner.com
                norbert.cerner.com/MCS_application: mlworkflowevents
                norbert.cerner.com/MCS_project: alva
                norbert.cerner.com/MCS_region: open-kc-k8s-asp-mid-0
                norbert.cerner.com/MCS_stack: staging
                norbert.cerner.com/MCS_tenant: stgeng-temp-rho-cernerasp-com
                norbert.cerner.com/com.cerner.repo_sha: 9e89d26c529bb23ccb948930ca6c0a359f039979
                norbert.cerner.com/com.cerner.repo_url:
                  https://raw.github.cerner.com/alva/alva-config/add5f517015b2f995970883eab96de2eb2c9880d/docs/ml-workflow-events.yaml
                norbert.cerner.com/splunk-index: alva
                norbert.cerner.com/splunk-source: alva:mlworkflowevents:staging:open-kc-k8s-asp-mid-0:stgeng-temp-rho-cernerasp-com:1.5-20201211T204430Z
  Init Containers:
   ca-certs-jks:
    Image:      docker-production.cernerrepos.net/norbert/ca-certs-client:v0.4.1
    Port:       <none>
    Host Port:  <none>
    Environment:
      CERNER_CA_CERT_BUNDLE:  alva-ca-certificates.jks
    Mounts:
      /mnt/ca-certs from cacerts-volume (rw)
   ca-certs-pem:
    Image:      docker-production.cernerrepos.net/norbert/ca-certs-client:v0.4.1
    Port:       <none>
    Host Port:  <none>
    Environment:
      CERNER_CA_CERT_BUNDLE:  alva-ca-certificates.pem
    Mounts:
      /mnt/ca-certs from cacerts-volume (rw)
   map-secrets:
    Image:      docker.cernerrepos.net/busybox:1.31.1
    Port:       <none>
    Host Port:  <none>
    Command:
      /scripts/appendsecrets.sh
      /input/config.properties
      /output/config.properties
      /secrets
      -m
      alva.environment.entry.cerner/oauth/millennium/consumer-key.value
      staging.consumer-key
      -m
      alva.environment.entry.cerner/oauth/millennium/consumer-secret.value
      staging.consumer-secret
    Environment:  <none>
    Mounts:
      /input from config-volume (rw)
      /output from workdir (rw)
      /scripts from script (rw)
      /secrets/staging.consumer-key/ from staging-consumer-key (rw)
      /secrets/staging.consumer-secret/ from staging-consumer-secret (rw)
  Containers:
   mlworkflowevents:
    Image:       docker-integration.cernerrepos.net/alva/ml-workflow-events:1.5-20201211T204430Z
    Ports:       8444/TCP, 8443/TCP
    Host Ports:  0/TCP, 0/TCP
    Limits:
      memory:  1264Mi
    Requests:
      cpu:      70m
      memory:   1264Mi
    Liveness:   http-get https://:main/meta/availability delay=600s timeout=10s period=30s #success=1 #failure=3
    Readiness:  http-get https://:main/meta/health delay=0s timeout=10s period=30s #success=1 #failure=3
    Environment Variables from:
      mlworkflowevents-staging-stgeng-temp-rho-cernerasp-com-config-v007  ConfigMap  Optional: false
    Environment:
      NEW_RELIC_METADATA_KUBERNETES_CLUSTER_NAME:          open-kc-k8s-asp-mid-0
      NEW_RELIC_METADATA_KUBERNETES_NODE_NAME:              (v1:spec.nodeName)
      NEW_RELIC_METADATA_KUBERNETES_NAMESPACE_NAME:         (v1:metadata.namespace)
      NEW_RELIC_METADATA_KUBERNETES_DEPLOYMENT_NAME:        (v1:metadata.annotations['artifact.spinnaker.io/name'])
      NEW_RELIC_METADATA_KUBERNETES_POD_NAME:               (v1:metadata.name)
      NEW_RELIC_METADATA_KUBERNETES_CONTAINER_NAME:         (v1:metadata.annotations['moniker.spinnaker.io/application'])
      NEW_RELIC_METADATA_KUBERNETES_CONTAINER_IMAGE_NAME:  docker-integration.cernerrepos.net/alva/ml-workflow-events:1.5-20201211T204430Z
      NEW_RELIC_LICENSE_KEY:                               <set to the key 'value' in secret 'staging.new-relic-license-key'>      Optional: false
      alva.client.alva-ml-config.token:                    <set to the key 'value' in secret 'staging.auth-bearer-token'>          Optional: false
      alva.oauthsigner.oauth1.secret:                      <set to the key 'value' in secret 'staging.oauthsigner-oauth1-secret'>  Optional: false
    Mounts:
      /opt/alva/ca-certs from cacerts-volume (rw)
      /opt/alva/conf from workdir (rw)
      /tmp/alva/ from temp-storage (rw)
  Volumes:
   cacerts-volume:
    Type:       EmptyDir (a temporary directory that shares a pod's lifetime)
    Medium:
    SizeLimit:  <unset>
   config-volume:
    Type:      ConfigMap (a volume populated by a ConfigMap)
    Name:      mlworkflowevents-staging-stgeng-temp-rho-cernerasp-com-config-file-v001
    Optional:  false
   workdir:
    Type:       EmptyDir (a temporary directory that shares a pod's lifetime)
    Medium:
    SizeLimit:  <unset>
   script:
    Type:      ConfigMap (a volume populated by a ConfigMap)
    Name:      appendsecrets-script-configmap-v000
    Optional:  false
   temp-storage:
    Type:       EmptyDir (a temporary directory that shares a pod's lifetime)
    Medium:
    SizeLimit:  <unset>
   staging-consumer-key:
    Type:        Secret (a volume populated by a Secret)
    SecretName:  staging.consumer-key
    Optional:    false
   staging-consumer-secret:
    Type:               Secret (a volume populated by a Secret)
    SecretName:         staging.consumer-secret
    Optional:           false
  Priority Class Name:  medium
Events:                 <none>
```

