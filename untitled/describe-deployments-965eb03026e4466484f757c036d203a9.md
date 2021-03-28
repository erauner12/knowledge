# describe deployments 965eb03026e4466484f757c036d203a9

```bash
er046256@w1738944  ~/tmp/Container-Masterclass-Codes/CC_Kubernetes/S12  kubectl describe deployment mlallergyreference-production-p205-sgen-oh-cernerasp-com
Name:                   mlallergyreference-production-p205-sgen-oh-cernerasp-com
Namespace:              alva-prod
CreationTimestamp:      Tue, 21 May 2019 13:11:08 -0500
Labels:                 app.kubernetes.io/managed-by=spinnaker
                        app.kubernetes.io/name=mlallergyreference
                        norbert.cerner.com/application=mlallergyreference
                        norbert.cerner.com/helm=0.2.0-2b1f052-20200617T105933Z
                        norbert.cerner.com/project=alva
                        norbert.cerner.com/region=open-kc-k8s-asp-mid-0
                        norbert.cerner.com/stack=production
                        norbert.cerner.com/tenant=p205-sgen-oh-cernerasp-com
Annotations:            artifact.spinnaker.io/location: alva-prod
                        artifact.spinnaker.io/name: mlallergyreference-production-p205-sgen-oh-cernerasp-com
                        artifact.spinnaker.io/type: kubernetes/deployment
                        deployment.kubernetes.io/revision: 39
                        moniker.spinnaker.io/application: mlallergyreference
                        moniker.spinnaker.io/cluster: mlallergyreference-production-p205-sgen-oh-cernerasp-com
                        moniker.spinnaker.io/detail: -p205-sgen-oh-cernerasp-com
                        moniker.spinnaker.io/stack: production
                        norbert.cerner.com/MCS_POINTS_OF_CONTACT: jswoboda@cerner.com,dinesh.bajracharya@cerner.com,pavani.gorantla@cerner.com
                        norbert.cerner.com/MCS_application: mlallergyreference
                        norbert.cerner.com/MCS_project: alva
                        norbert.cerner.com/MCS_region: open-kc-k8s-asp-mid-0
                        norbert.cerner.com/MCS_stack: production
                        norbert.cerner.com/MCS_tenant: p205-sgen-oh-cernerasp-com
                        norbert.cerner.com/com.cerner.repo_sha: 18eb9bdc49f6b1effd2be8b44232e15382eab69c
                        norbert.cerner.com/com.cerner.repo_url:
                          https://raw.github.cerner.com/alva/alva-config/9848401497aecc1fa3b617a8684f09f8fd2ea468/docs/ml-allergy-reference.yaml
                        norbert.cerner.com/splunk-index: alva
                        norbert.cerner.com/splunk-source: docker-production.cernerrepos.net/alva/ml-allergy-reference:0.5-20201110T014448Z
Selector:               norbert.cerner.com/application=mlallergyreference,norbert.cerner.com/project=alva,norbert.cerner.com/region=open-kc-k8s-asp-mid-0,norbert.cerner.com/stack=production,norbert.cerner.com/tenant=p205-sgen-oh-cernerasp-com
Replicas:               2 desired | 2 updated | 2 total | 2 available | 0 unavailable
StrategyType:           RollingUpdate
MinReadySeconds:        0
RollingUpdateStrategy:  25% max unavailable, 25% max surge
Pod Template:
  Labels:       app.kubernetes.io/managed-by=spinnaker
                app.kubernetes.io/name=mlallergyreference
                norbert.cerner.com/application=mlallergyreference
                norbert.cerner.com/consume-alva-eureka-production-us-asp-kc-8a-main=true
                norbert.cerner.com/consume-alva-eureka-production-us-asp-kc-8b-main=true
                norbert.cerner.com/consume-alva-eureka-production-us-asp-kc-8c-main=true
                norbert.cerner.com/consume-alva-mlconfig-production-main=true
                norbert.cerner.com/consume-alva-mlwebtoken-production-p205-sgen-ohc3e6cfddf093b6ac=true
                norbert.cerner.com/exposeTo-alva-edge-production=true
                norbert.cerner.com/exposeTo-alva-watt-production=true
                norbert.cerner.com/external-10.30.4.101=true
                norbert.cerner.com/external-149.45.12.15=true
                norbert.cerner.com/external-161.130.11.170=true
                norbert.cerner.com/external-170.71.223.166=true
                norbert.cerner.com/external-antivirus-service.cernerpowerchart.net=true
                norbert.cerner.com/external-cernabcneaodr01.cernerasp.com=true
                norbert.cerner.com/external-cernabcneaodr03.cernerasp.com=true
                norbert.cerner.com/external-cernabcneaodr05.cernerasp.com=true
                norbert.cerner.com/external-cernabcneaodr06.cernerasp.com=true
                norbert.cerner.com/external-cernabcneaodr09.cernerasp.com=true
                norbert.cerner.com/external-cernabcneaodr11.cernerasp.com=true
                norbert.cerner.com/external-cernhecnas.cernerasp.com=true
                norbert.cerner.com/external-mill-alva-test.api.healtheintent.com=true
                norbert.cerner.com/external-new-relic=true
                norbert.cerner.com/external-pod002-distcache-test-ls-cachenode-001.cernerasp.com=true
                norbert.cerner.com/external-pod002-distcache-test-ls-cachenode-002.cernerasp.com=true
                norbert.cerner.com/external-pod002-distcache-test-ls-cachenode-003.cernerasp.com=true
                norbert.cerner.com/external-production-base-network=true
                norbert.cerner.com/external-taspmogseftc10.cernerasp.com=true
                norbert.cerner.com/external-temprhoeaodr03.cernerasp.com=true
                norbert.cerner.com/external-tmprhoctx67.cmsext.com=true
                norbert.cerner.com/external-univmoapp1.cernerasp.com=true
                norbert.cerner.com/external-univmoapp2.cernerasp.com=true
                norbert.cerner.com/external-univmoapp3.cernerasp.com=true
                norbert.cerner.com/external-univmoapp4.cernerasp.com=true
                norbert.cerner.com/external-univmoapp8.cernerasp.com=true
                norbert.cerner.com/external-univmoapp9.cernerasp.com=true
                norbert.cerner.com/external-univmonas.cernerasp.com=true
                norbert.cerner.com/helm=0.2.0-2b1f052-20200617T105933Z
                norbert.cerner.com/profile=alva-mlallergyreference-production-p205-sgen-oh-cernerasp-com
                norbert.cerner.com/project=alva
                norbert.cerner.com/region=open-kc-k8s-asp-mid-0
                norbert.cerner.com/stack=production
                norbert.cerner.com/tenant=p205-sgen-oh-cernerasp-com
  Annotations:  artifact.spinnaker.io/location: alva-prod
                artifact.spinnaker.io/name: mlallergyreference-production-p205-sgen-oh-cernerasp-com
                artifact.spinnaker.io/type: kubernetes/deployment
                moniker.spinnaker.io/application: mlallergyreference
                moniker.spinnaker.io/cluster: mlallergyreference-production-p205-sgen-oh-cernerasp-com
                moniker.spinnaker.io/detail: -p205-sgen-oh-cernerasp-com
                moniker.spinnaker.io/stack: production
                norbert.cerner.com/MCS_POINTS_OF_CONTACT: jswoboda@cerner.com,dinesh.bajracharya@cerner.com,pavani.gorantla@cerner.com
                norbert.cerner.com/MCS_application: mlallergyreference
                norbert.cerner.com/MCS_project: alva
                norbert.cerner.com/MCS_region: open-kc-k8s-asp-mid-0
                norbert.cerner.com/MCS_stack: production
                norbert.cerner.com/MCS_tenant: p205-sgen-oh-cernerasp-com
                norbert.cerner.com/com.cerner.repo_sha: 18eb9bdc49f6b1effd2be8b44232e15382eab69c
                norbert.cerner.com/com.cerner.repo_url:
                  https://raw.github.cerner.com/alva/alva-config/9848401497aecc1fa3b617a8684f09f8fd2ea468/docs/ml-allergy-reference.yaml
                norbert.cerner.com/splunk-index: alva
                norbert.cerner.com/splunk-source: alva:mlallergyreference:production:open-kc-k8s-asp-mid-0:p205-sgen-oh-cernerasp-com:0.5-20201110T014448Z
  Init Containers:
   ca-certs:
    Image:      docker-production.cernerrepos.net/norbert/ca-certs-client:v0.4.1
    Port:       <none>
    Host Port:  <none>
    Environment:
      CERNER_CA_CERT_BUNDLE:  alva-ca-certificates.jks
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
      production.consumer-key
      -m
      alva.environment.entry.cerner/oauth/millennium/consumer-secret.value
      production.consumer-secret
    Environment:  <none>
    Mounts:
      /input from config-volume (rw)
      /output from workdir (rw)
      /scripts from script (rw)
      /secrets/production.consumer-key/ from production-consumer-key (rw)
      /secrets/production.consumer-secret/ from production-consumer-secret (rw)
  Containers:
   mlallergyreference:
    Image:       docker-production.cernerrepos.net/alva/ml-allergy-reference:0.5-20201110T014448Z
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
      mlallergyreference-production-p205-sgen-oh-cernerasp-com-config-v047  ConfigMap  Optional: false
    Environment:
      NEW_RELIC_METADATA_KUBERNETES_CLUSTER_NAME:          open-kc-k8s-asp-mid-0
      NEW_RELIC_METADATA_KUBERNETES_NODE_NAME:              (v1:spec.nodeName)
      NEW_RELIC_METADATA_KUBERNETES_NAMESPACE_NAME:         (v1:metadata.namespace)
      NEW_RELIC_METADATA_KUBERNETES_DEPLOYMENT_NAME:        (v1:metadata.annotations['artifact.spinnaker.io/name'])
      NEW_RELIC_METADATA_KUBERNETES_POD_NAME:               (v1:metadata.name)
      NEW_RELIC_METADATA_KUBERNETES_CONTAINER_NAME:         (v1:metadata.annotations['moniker.spinnaker.io/application'])
      NEW_RELIC_METADATA_KUBERNETES_CONTAINER_IMAGE_NAME:  docker-production.cernerrepos.net/alva/ml-allergy-reference:0.5-20201110T014448Z
      NEW_RELIC_LICENSE_KEY:                               <set to the key 'value' in secret 'production.new-relic-license-key'>      Optional: false
      alva.client.alva-ml-config.token:                    <set to the key 'value' in secret 'production.auth-bearer-token'>          Optional: false
      alva.oauthsigner.oauth1.secret:                      <set to the key 'value' in secret 'production.oauthsigner-oauth1-secret'>  Optional: false
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
    Name:      mlallergyreference-production-p205-sgen-oh-cernerasp-com-config-file-v001
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
   production-consumer-key:
    Type:        Secret (a volume populated by a Secret)
    SecretName:  production.consumer-key
    Optional:    false
   production-consumer-secret:
    Type:               Secret (a volume populated by a Secret)
    SecretName:         production.consumer-secret
    Optional:           false
  Priority Class Name:  medium
Conditions:
  Type           Status  Reason
  ----           ------  ------
  Progressing    True    NewReplicaSetAvailable
  Available      True    MinimumReplicasAvailable
OldReplicaSets:  mlallergyreference-production-p205-sgen-oh-cernerasp-com-89b46d5c8 (2/2 replicas created)
NewReplicaSet:   <none>
Events:          <none>
```

```bash
Selector:               norbert.cerner.com/application=mlallergyreference,norbert.cerner.com/project=alva,norbert.cerner.com/region=open-kc-k8s-asp-mid-0,norbert.cerner.com/stack=production,norbert.cerner.com/tenant=p205-sgen-oh-cernerasp-com
Replicas:               2 desired | 2 updated | 2 total | 2 available | 0 unavailable
StrategyType:           RollingUpdate
```

```bash
Labels:       app.kubernetes.io/managed-by=spinnaker
                app.kubernetes.io/name=mlallergyreference
                norbert.cerner.com/application=mlallergyreference
                norbert.cerner.com/consume-alva-eureka-production-us-asp-kc-8a-main=true
                norbert.cerner.com/consume-alva-eureka-production-us-asp-kc-8b-main=true
                norbert.cerner.com/consume-alva-eureka-production-us-asp-kc-8c-main=true
                norbert.cerner.com/consume-alva-mlconfig-production-main=true
                norbert.cerner.com/consume-alva-mlwebtoken-production-p205-sgen-ohc3e6cfddf093b6ac=true
                norbert.cerner.com/exposeTo-alva-edge-production=true
                norbert.cerner.com/exposeTo-alva-watt-production=true
                norbert.cerner.com/external-10.30.4.101=true
                norbert.cerner.com/external-149.45.12.15=true
                norbert.cerner.com/external-161.130.11.170=true
                norbert.cerner.com/external-170.71.223.166=true
                norbert.cerner.com/external-antivirus-service.cernerpowerchart.net=true
                norbert.cerner.com/external-cernabcneaodr01.cernerasp.com=true
                norbert.cerner.com/external-cernabcneaodr03.cernerasp.com=true
                norbert.cerner.com/external-cernabcneaodr05.cernerasp.com=true
                norbert.cerner.com/external-cernabcneaodr06.cernerasp.com=true
                norbert.cerner.com/external-cernabcneaodr09.cernerasp.com=true
                norbert.cerner.com/external-cernabcneaodr11.cernerasp.com=true
                norbert.cerner.com/external-cernhecnas.cernerasp.com=true
                norbert.cerner.com/external-mill-alva-test.api.healtheintent.com=true
                norbert.cerner.com/external-new-relic=true
                norbert.cerner.com/external-pod002-distcache-test-ls-cachenode-001.cernerasp.com=true
                norbert.cerner.com/external-pod002-distcache-test-ls-cachenode-002.cernerasp.com=true
                norbert.cerner.com/external-pod002-distcache-test-ls-cachenode-003.cernerasp.com=true
                norbert.cerner.com/external-production-base-network=true
                norbert.cerner.com/external-taspmogseftc10.cernerasp.com=true
                norbert.cerner.com/external-temprhoeaodr03.cernerasp.com=true
                norbert.cerner.com/external-tmprhoctx67.cmsext.com=true
                norbert.cerner.com/external-univmoapp1.cernerasp.com=true
                norbert.cerner.com/external-univmoapp2.cernerasp.com=true
                norbert.cerner.com/external-univmoapp3.cernerasp.com=true
                norbert.cerner.com/external-univmoapp4.cernerasp.com=true
                norbert.cerner.com/external-univmoapp8.cernerasp.com=true
                norbert.cerner.com/external-univmoapp9.cernerasp.com=true
                norbert.cerner.com/external-univmonas.cernerasp.com=true
                norbert.cerner.com/helm=0.2.0-2b1f052-20200617T105933Z
                norbert.cerner.com/profile=alva-mlallergyreference-production-p205-sgen-oh-cernerasp-com
                norbert.cerner.com/project=alva
                norbert.cerner.com/region=open-kc-k8s-asp-mid-0
                norbert.cerner.com/stack=production
                norbert.cerner.com/tenant=p205-sgen-oh-cernerasp-com
```

