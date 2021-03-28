# Deployments 08c1ca47b16d4df19deacaa7cc7a85ca

## Deployments

## Overview

* Higher unit of orchestration. Higher than ods and ReplicaSets
* used to create pods, manages replicas, attach services, rollout updates
* Uses labels and selectors to identify pods and pod template
* Used for deploying stateless applications
* Most widely used

```yaml
apiVersion: apps/v1 
kind: Deployment
metadata:
  name: deploy-nginx
spec:
  selector:
    matchLabels:
      app: nginx
  replicas: 2 
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: deploy-container
        image: nginx:1.7.9
        ports:
        - containerPort: 80
```

* `replicas`

```yaml
er046256@w1738944  ~/tmp/Container-Masterclass-Codes/CC_Kubernetes/S10  kubectl get deployments
NAME           READY   UP-TO-DATE   AVAILABLE   AGE
deploy-nginx   2/2     2            2           3m18s
```

```yaml
er046256@w1738944  ~/tmp/Container-Masterclass-Codes/CC_Kubernetes/S10  kgp
NAME                            READY   STATUS              RESTARTS   AGE
deploy-nginx-54b8848497-gb62w   0/1     ContainerCreating   0          6s
deploy-nginx-54b8848497-tspkj   0/1     ContainerCreating   0          6s
```

```yaml
er046256@w1738944  ~/tmp/Container-Masterclass-Codes/CC_Kubernetes/S10  kubectl describe deployments deploy-nginx
Name:                   deploy-nginx
Namespace:              default
CreationTimestamp:      Sat, 09 Jan 2021 17:30:15 -0600
Labels:                 <none>
Annotations:            deployment.kubernetes.io/revision: 1
Selector:               app=nginx
Replicas:               2 desired | 2 updated | 2 total | 2 available | 0 unavailable
StrategyType:           RollingUpdate
MinReadySeconds:        0
RollingUpdateStrategy:  25% max unavailable, 25% max surge
Pod Template:
  Labels:  app=nginx
  Containers:
   deploy-container:
    Image:        nginx:1.7.9
    Port:         80/TCP
    Host Port:    0/TCP
    Environment:  <none>
    Mounts:       <none>
  Volumes:        <none>
Conditions:
  Type           Status  Reason
  ----           ------  ------
  Available      True    MinimumReplicasAvailable
  Progressing    True    NewReplicaSetAvailable
OldReplicaSets:  <none>
NewReplicaSet:   deploy-nginx-54b8848497 (2/2 replicas created)
Events:
  Type    Reason             Age    From                   Message
  ----    ------             ----   ----                   -------
  Normal  ScalingReplicaSet  3m54s  deployment-controller  Scaled up replica set deploy-nginx-54b8848497 to 2
```

```yaml
Name:         deploy-nginx-54b8848497-gb62w
Namespace:    default
Priority:     0
Node:         docker-desktop/192.168.65.3
Start Time:   Sat, 09 Jan 2021 17:30:15 -0600
Labels:       app=nginx
              pod-template-hash=54b8848497
Annotations:  <none>
Status:       Running
IP:           10.1.0.18
IPs:
  IP:           10.1.0.18
Controlled By:  ReplicaSet/deploy-nginx-54b8848497
Containers:
  deploy-container:
    Container ID:   docker://5248c213796f8ee9858827d93e12642888dc94c893b788ff858fd1c350883570
    Image:          nginx:1.7.9
    Image ID:       docker-pullable://nginx@sha256:e3456c851a152494c3e4ff5fcc26f240206abac0c9d794affb40e0714846c451
    Port:           80/TCP
    Host Port:      0/TCP
    State:          Running
      Started:      Sat, 09 Jan 2021 17:30:26 -0600
    Ready:          True
    Restart Count:  0
    Environment:    <none>
    Mounts:
      /var/run/secrets/kubernetes.io/serviceaccount from default-token-q4hf6 (ro)
Conditions:
  Type              Status
  Initialized       True
  Ready             True
  ContainersReady   True
  PodScheduled      True
Volumes:
  default-token-q4hf6:
    Type:        Secret (a volume populated by a Secret)
    SecretName:  default-token-q4hf6
    Optional:    false
QoS Class:       BestEffort
Node-Selectors:  <none>
Tolerations:     node.kubernetes.io/not-ready:NoExecute op=Exists for 300s
                 node.kubernetes.io/unreachable:NoExecute op=Exists for 300s
Events:
  Type    Reason     Age   From               Message
  ----    ------     ----  ----               -------
  Normal  Scheduled  101s  default-scheduler  Successfully assigned default/deploy-nginx-54b8848497-gb62w to docker-desktop
  Normal  Pulling    100s  kubelet            Pulling image "nginx:1.7.9"
  Normal  Pulled     91s   kubelet            Successfully pulled image "nginx:1.7.9" in 9.4771705s
  Normal  Created    91s   kubelet            Created container deploy-container
  Normal  Started    90s   kubelet            Started container deploy-container
```

`DeploymentUpdateStrategy`

* if a deployment has 4 pods
* 25% max unavailability = at least 3 pods
* 25% max surge = pod creation limit: 5 pods

`NewReplicaSet`

* the name of the replicaset that has been created for this deployment

