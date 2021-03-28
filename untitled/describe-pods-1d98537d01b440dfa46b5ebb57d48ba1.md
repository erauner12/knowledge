# Describe pods 1d98537d01b440dfa46b5ebb57d48ba1

```bash
er046256@w1738944  ~/tmp/Container-Masterclass-Codes/CC_Kubernetes/S12  kubectl describe pod mlappointment-production-p1751-flho-fl-cernerasp-com-84f744cwk9
Name:                 mlappointment-production-p1751-flho-fl-cernerasp-com-84f744cwk9
Namespace:            alva-prod
Priority:             10000
Priority Class Name:  medium
Node:                 k8s-asp-mid-us-asp-kc-8c-192-168-40-74.novalocal/192.168.40.74
Start Time:           Tue, 15 Dec 2020 17:10:06 -0600
Labels:               app.kubernetes.io/managed-by=spinnaker
                      app.kubernetes.io/name=mlappointment
                      norbert.cerner.com/application=mlappointment
                      norbert.cerner.com/consume-alva-eureka-production-us-asp-kc-8a-main=true
                      norbert.cerner.com/consume-alva-eureka-production-us-asp-kc-8b-main=true
                      norbert.cerner.com/consume-alva-eureka-production-us-asp-kc-8c-main=true
                      norbert.cerner.com/consume-alva-mlconfig-production-main=true
                      norbert.cerner.com/consume-alva-mlwebtoken-production-p1751-flho-f35b95ff62ebabf8c=true
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
                      norbert.cerner.com/helm=0.2.0-20201201T133842Z-1ccc6f1
                      norbert.cerner.com/profile=alva-mlappointment-production-p1751-flho-fl-cernerasp-com
                      norbert.cerner.com/project=alva
                      norbert.cerner.com/region=open-kc-k8s-asp-mid-0
                      norbert.cerner.com/stack=production
                      norbert.cerner.com/tenant=p1751-flho-fl-cernerasp-com
                      pod-template-hash=84f74756cf
Annotations:          artifact.spinnaker.io/location: alva-prod
                      artifact.spinnaker.io/name: mlappointment-production-p1751-flho-fl-cernerasp-com
                      artifact.spinnaker.io/type: kubernetes/deployment
                      cni.projectcalico.org/podIP: 172.17.113.122/32
                      cni.projectcalico.org/podIPs: 172.17.113.122/32
                      kubernetes.io/psp: consumer-allowroot-podsecuritypolicy
                      moniker.spinnaker.io/application: mlappointment
                      moniker.spinnaker.io/cluster: mlappointment-production-p1751-flho-fl-cernerasp-com
                      moniker.spinnaker.io/detail: -p1751-flho-fl-cernerasp-com
                      moniker.spinnaker.io/stack: production
                      norbert.cerner.com/MCS_POINTS_OF_CONTACT:
                        kriti.chakdar@cerner.com,kris.reks@cerner.com,zhuo.wang@cerner.com,caleb.miller@cerner.com,jacob.baute@cerner.com,xianlong.zhang@cerner.co...
                      norbert.cerner.com/MCS_application: mlappointment
                      norbert.cerner.com/MCS_project: alva
                      norbert.cerner.com/MCS_region: open-kc-k8s-asp-mid-0
                      norbert.cerner.com/MCS_stack: production
                      norbert.cerner.com/MCS_tenant: p1751-flho-fl-cernerasp-com
                      norbert.cerner.com/com.cerner.repo_sha: 4d0780b0497a046c6f0e9feba1124fb44d76ae44
                      norbert.cerner.com/com.cerner.repo_url:
                        https://raw.github.cerner.com/alva/alva-config/4d0780b0497a046c6f0e9feba1124fb44d76ae44/docs/ml-appointment.yaml
                      norbert.cerner.com/splunk-index: alva
                      norbert.cerner.com/splunk-source: alva:mlappointment:production:open-kc-k8s-asp-mid-0:p1751-flho-fl-cernerasp-com:9.14.0-20201119T121433Z
                      seccomp.security.alpha.kubernetes.io/pod: runtime/default
Status:               Running
IP:                   172.17.113.122
IPs:
  IP:           172.17.113.122
Controlled By:  ReplicaSet/mlappointment-production-p1751-flho-fl-cernerasp-com-84f74756cf
Init Containers:
  ca-certs-jks:
    Container ID:   docker://46730a4152c294d36a8fde1b44eaef718095c4e23cabe89ff78188ae0918849d
    Image:          docker-production.cernerrepos.net/norbert/ca-certs-client:v0.4.1
    Image ID:       docker-pullable://docker-production.cernerrepos.net/norbert/ca-certs-client@sha256:b965ddf388f5d0af9b546c7d1d8b19e556f600f260d600415ead51e404c4142b
    Port:           <none>
    Host Port:      <none>
    State:          Terminated
      Reason:       Completed
      Exit Code:    0
      Started:      Tue, 15 Dec 2020 17:10:08 -0600
      Finished:     Tue, 15 Dec 2020 17:10:11 -0600
    Ready:          True
    Restart Count:  0
    Environment:
      CERNER_CA_CERT_BUNDLE:  alva-ca-certificates.jks
    Mounts:
      /mnt/ca-certs from cacerts-volume (rw)
      /var/run/secrets/kubernetes.io/serviceaccount from default-token-kksm5 (ro)
  ca-certs-pem:
    Container ID:   docker://309b8d7b0eb5383d75e04126358dad0b620418e15ea4ab90988ca69368f6c6f4
    Image:          docker-production.cernerrepos.net/norbert/ca-certs-client:v0.4.1
    Image ID:       docker-pullable://docker-production.cernerrepos.net/norbert/ca-certs-client@sha256:b965ddf388f5d0af9b546c7d1d8b19e556f600f260d600415ead51e404c4142b
    Port:           <none>
    Host Port:      <none>
    State:          Terminated
      Reason:       Completed
      Exit Code:    0
      Started:      Tue, 15 Dec 2020 17:10:12 -0600
      Finished:     Tue, 15 Dec 2020 17:10:12 -0600
    Ready:          True
    Restart Count:  0
    Environment:
      CERNER_CA_CERT_BUNDLE:  alva-ca-certificates.pem
    Mounts:
      /mnt/ca-certs from cacerts-volume (rw)
      /var/run/secrets/kubernetes.io/serviceaccount from default-token-kksm5 (ro)
  map-secrets:
    Container ID:  docker://55a14efa83ce8aac5d882b260713ca9ee250f062b3df02cac9e7d5e47b4642f4
    Image:         docker.cernerrepos.net/busybox:1.31.1
    Image ID:      docker-pullable://docker.cernerrepos.net/busybox@sha256:afe605d272837ce1732f390966166c2afff5391208ddd57de10942748694049d
    Port:          <none>
    Host Port:     <none>
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
    State:          Terminated
      Reason:       Completed
      Exit Code:    0
      Started:      Tue, 15 Dec 2020 17:10:13 -0600
      Finished:     Tue, 15 Dec 2020 17:10:13 -0600
    Ready:          True
    Restart Count:  0
    Environment:    <none>
    Mounts:
      /input from config-volume (rw)
      /output from workdir (rw)
      /scripts from script (rw)
      /secrets/production.consumer-key/ from production-consumer-key (rw)
      /secrets/production.consumer-secret/ from production-consumer-secret (rw)
      /var/run/secrets/kubernetes.io/serviceaccount from default-token-kksm5 (ro)
Containers:
  mlappointment:
    Container ID:   docker://fa507136426eda910a668f47301222842c4809537b2a132e975e7434ea5a6c02
    Image:          docker-production.cernerrepos.net/alva/ml-appointment:9.14.0-20201119T121433Z
    Image ID:       docker-pullable://docker-production.cernerrepos.net/alva/ml-appointment@sha256:1723709e55d7b17e7b2ec4d850d6c73845a8469a9969a4d67ce6ba4ef3d6d6ce
    Ports:          8444/TCP, 8443/TCP
    Host Ports:     0/TCP, 0/TCP
    State:          Running
      Started:      Tue, 15 Dec 2020 17:10:56 -0600
    Ready:          True
    Restart Count:  0
    Limits:
      memory:  1264Mi
    Requests:
      cpu:      70m
      memory:   1264Mi
    Liveness:   http-get https://:main/meta/availability delay=600s timeout=10s period=30s #success=1 #failure=3
    Readiness:  http-get https://:main/meta/health delay=0s timeout=10s period=30s #success=1 #failure=3
    Environment Variables from:
      mlappointment-production-p1751-flho-fl-cernerasp-com-config-v005  ConfigMap  Optional: false
    Environment:
      NEW_RELIC_METADATA_KUBERNETES_CLUSTER_NAME:          open-kc-k8s-asp-mid-0
      NEW_RELIC_METADATA_KUBERNETES_NODE_NAME:              (v1:spec.nodeName)
      NEW_RELIC_METADATA_KUBERNETES_NAMESPACE_NAME:        alva-prod (v1:metadata.namespace)
      NEW_RELIC_METADATA_KUBERNETES_DEPLOYMENT_NAME:        (v1:metadata.annotations['artifact.spinnaker.io/name'])
      NEW_RELIC_METADATA_KUBERNETES_POD_NAME:              mlappointment-production-p1751-flho-fl-cernerasp-com-84f744cwk9 (v1:metadata.name)
      NEW_RELIC_METADATA_KUBERNETES_CONTAINER_NAME:         (v1:metadata.annotations['moniker.spinnaker.io/application'])
      NEW_RELIC_METADATA_KUBERNETES_CONTAINER_IMAGE_NAME:  docker-production.cernerrepos.net/alva/ml-appointment:9.14.0-20201119T121433Z
      NEW_RELIC_LICENSE_KEY:                               <set to the key 'value' in secret 'production.new-relic-license-key'>      Optional: false
      alva.client.alva-ml-config.token:                    <set to the key 'value' in secret 'production.auth-bearer-token'>          Optional: false
      alva.oauthsigner.oauth1.secret:                      <set to the key 'value' in secret 'production.oauthsigner-oauth1-secret'>  Optional: false
    Mounts:
      /opt/alva/ca-certs from cacerts-volume (rw)
      /opt/alva/conf from workdir (rw)
      /tmp/alva/ from temp-storage (rw)
      /var/run/secrets/kubernetes.io/serviceaccount from default-token-kksm5 (ro)
Conditions:
  Type              Status
  Initialized       True
  Ready             True
  ContainersReady   True
  PodScheduled      True
Volumes:
  cacerts-volume:
    Type:       EmptyDir (a temporary directory that shares a pod's lifetime)
    Medium:
    SizeLimit:  <unset>
  config-volume:
    Type:      ConfigMap (a volume populated by a ConfigMap)
    Name:      mlappointment-production-p1751-flho-fl-cernerasp-com-config-file-v000
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
    Type:        Secret (a volume populated by a Secret)
    SecretName:  production.consumer-secret
    Optional:    false
  default-token-kksm5:
    Type:        Secret (a volume populated by a Secret)
    SecretName:  default-token-kksm5
    Optional:    false
QoS Class:       Burstable
Node-Selectors:  <none>
Tolerations:     node.kubernetes.io/not-ready:NoExecute op=Exists for 30s
                 node.kubernetes.io/unreachable:NoExecute op=Exists for 30s
Events:          <none>
```

