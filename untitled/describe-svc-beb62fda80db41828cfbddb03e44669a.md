# describe svc beb62fda80db41828cfbddb03e44669a

```bash
er046256@w1738944  ~/tmp/Container-Masterclass-Codes/CC_Kubernetes/S12  kubectl get svc
NAME                                                              TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)    AGE
edge-production-service                                           ClusterIP   172.24.77.29     <none>        8443/TCP   701d
edge-sandbox-service                                              ClusterIP   172.24.60.180    <none>        8443/TCP   723d
edge-staging-service                                              ClusterIP   172.24.235.93    <none>        8443/TCP   723d
eureka-production-us-asp-kc-8a-service                            ClusterIP   172.24.68.195    <none>        8080/TCP   701d
eureka-production-us-asp-kc-8b-service                            ClusterIP   172.24.212.239   <none>        8080/TCP   701d
eureka-production-us-asp-kc-8c-service                            ClusterIP   172.24.214.20    <none>        8080/TCP   701d
eureka-sandbox-us-asp-kc-8a-service                               ClusterIP   172.24.189.249   <none>        8080/TCP   723d
eureka-sandbox-us-asp-kc-8b-service                               ClusterIP   172.24.201.159   <none>        8080/TCP   723d
eureka-sandbox-us-asp-kc-8c-service                               ClusterIP   172.24.179.11    <none>        8080/TCP   723d
eureka-staging-us-asp-kc-8a-service                               ClusterIP   172.24.77.49     <none>        8080/TCP   723d
eureka-staging-us-asp-kc-8b-service                               ClusterIP   172.24.50.79     <none>        8080/TCP   723d
eureka-staging-us-asp-kc-8c-service                               ClusterIP   172.24.150.190   <none>        8080/TCP   723d
mlallergy-prdeng-temp-rho-cernerasp-com                           ClusterIP   172.24.3.128     <none>        8443/TCP   135d
mlallergy-sndeng-temp-rho-cernerasp-com                           ClusterIP   172.24.137.234   <none>        8443/TCP   143d
mlallergy-staging-stgeng-temp-rho-cernerasp-com-service           ClusterIP   172.24.170.104   <none>        8443/TCP   484d
mlallergy-stgeng-temp-rho-cernerasp-com                           ClusterIP   172.24.155.163   <none>        8443/TCP   423d
mlautotext-prdeng-temp-rho-cernerasp-com                          ClusterIP   172.24.40.3      <none>        8443/TCP   135d
mlautotext-sndeng-temp-rho-cernerasp-com                          ClusterIP   172.24.106.149   <none>        8443/TCP   143d
mlautotext-stgeng-temp-rho-cernerasp-com                          ClusterIP   172.24.65.115    <none>        8443/TCP   325d
mlcareconcepts-prdeng-temp-rho-cernerasp-com                      ClusterIP   172.24.4.118     <none>        8443/TCP   81d
mlcareconcepts-sndeng-temp-rho-cernerasp-com                      ClusterIP   172.24.100.92    <none>        8443/TCP   86d
mlcareconcepts-stgeng-temp-rho-cernerasp-com                      ClusterIP   172.24.242.239   <none>        8443/TCP   219d
mlccd-prdeng-temp-rho-cernerasp-com                               ClusterIP   172.24.99.196    <none>        8443/TCP   135d
mlccd-sndeng-temp-rho-cernerasp-com                               ClusterIP   172.24.0.63      <none>        8443/TCP   143d
mlccd-staging-stgeng-temp-rho-cernerasp-com-service               ClusterIP   172.24.131.196   <none>        8443/TCP   508d
mlccd-stgeng-temp-rho-cernerasp-com                               ClusterIP   172.24.149.55    <none>        8443/TCP   422d
mlclinicalnote-prdeng-temp-rho-cernerasp-com                      ClusterIP   172.24.177.189   <none>        8443/TCP   135d
mlclinicalnote-sndeng-temp-rho-cernerasp-com                      ClusterIP   172.24.242.10    <none>        8443/TCP   143d
mlclinicalnote-stgeng-temp-rho-cernerasp-com                      ClusterIP   172.24.23.117    <none>        8443/TCP   298d
mlclinicalreportingadhoc-stgeng-temp-rho-cernerasp-com            ClusterIP   172.24.127.237   <none>        8443/TCP   102d
mlclinicalreportingdocservice-stgeng-temp-rho-cernerasp-com       ClusterIP   172.24.255.31    <none>        8443/TCP   102d
mlcondition-prdeng-temp-rho-cernerasp-com                         ClusterIP   172.24.148.66    <none>        8443/TCP   135d
mlcondition-sndeng-temp-rho-cernerasp-com                         ClusterIP   172.24.74.15     <none>        8443/TCP   143d
mlcondition-staging-stgeng-temp-rho-cernerasp-com-service         ClusterIP   172.24.214.142   <none>        8443/TCP   484d
mlcondition-stgeng-temp-rho-cernerasp-com                         ClusterIP   172.24.197.6     <none>        8443/TCP   422d
mlconfig-production-service                                       ClusterIP   172.24.214.216   <none>        8443/TCP   701d
mlconfig-sandbox-service                                          ClusterIP   172.24.196.33    <none>        8443/TCP   723d
mlconfig-staging-service                                          ClusterIP   172.24.152.147   <none>        8443/TCP   723d
mlconsumermessaginglegacy-prdeng-temp-rho-cernerasp-com           ClusterIP   172.24.146.237   <none>        8443/TCP   135d
mlconsumermessaginglegacy-sndeng-temp-rho-cernerasp-com           ClusterIP   172.24.85.110    <none>        8443/TCP   143d
mlconsumermessaginglegacy-staging-stgeng-temp-raa1431af027f131f   ClusterIP   172.24.183.52    <none>        8443/TCP   508d
mlconsumermessaginglegacy-staging-stgeng-temp-rad2ada8f0d1ba410   ClusterIP   172.24.174.250   <none>        8443/TCP   446d
mlconsumermessaginglegacy-stgeng-temp-rho-cernerasp-com           ClusterIP   172.24.75.33     <none>        8443/TCP   422d
mldemographicsclinical-prdeng-temp-rho-cernerasp-com              ClusterIP   172.24.56.242    <none>        8443/TCP   135d
mldemographicsclinical-sndeng-temp-rho-cernerasp-com              ClusterIP   172.24.166.39    <none>        8443/TCP   143d
mldemographicsclinical-staging-stgeng-temp-rho-030cf3aa5b16ae70   ClusterIP   172.24.127.172   <none>        8443/TCP   479d
mldemographicsclinical-staging-stgeng-temp-rho-f02df5310424263c   ClusterIP   172.24.222.167   <none>        8443/TCP   446d
mldemographicsclinical-stgeng-temp-rho-cernerasp-com              ClusterIP   172.24.235.0     <none>        8443/TCP   422d
mldiagnosisassistant-prdeng-temp-rho-cernerasp-com                ClusterIP   172.24.231.255   <none>        8443/TCP   135d
mldiagnosisassistant-sndeng-temp-rho-cernerasp-com                ClusterIP   172.24.200.190   <none>        8443/TCP   143d
mldiagnosisassistant-stgeng-temp-rho-cernerasp-com                ClusterIP   172.24.32.254    <none>        8443/TCP   263d
mldocument-prdeng-temp-rho-cernerasp-com                          ClusterIP   172.24.111.160   <none>        8443/TCP   135d
mldocument-sndeng-temp-rho-cernerasp-com                          ClusterIP   172.24.239.165   <none>        8443/TCP   143d
mldocument-staging-stgeng-temp-rho-cernerasp-com-service          ClusterIP   172.24.86.169    <none>        8443/TCP   479d
mldocument-stgeng-temp-rho-cernerasp-com                          ClusterIP   172.24.79.107    <none>        8443/TCP   422d
mldocumentcomponent-prdeng-temp-rho-cernerasp-com                 ClusterIP   172.24.158.88    <none>        8443/TCP   135d
mldocumentcomponent-sndeng-temp-rho-cernerasp-com                 ClusterIP   172.24.158.15    <none>        8443/TCP   1
```

