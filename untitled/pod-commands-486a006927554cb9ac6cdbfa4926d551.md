# Pod Commands 486a006927554cb9ac6cdbfa4926d551

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: cmd-pod
  labels:
    #sensible label
    purpose: demonstrate-command
spec:
  containers:
  - name: cmd-container
    #debian image
    image: debian
    # Here, instead of keeping the container up by running a loop of bash command,
    # We are just asking it to print a couple of environment variables which can be
    # verified with logs
    command: ["printenv"]
    args: ["HOSTNAME", "KUBERNETES_PORT"]
    restartPolicy: OnFailure
```

```yaml
kubectl create -f command-pod.yaml.yaml
```

```yaml
er046256@w1738944  ~/tmp/Container-Masterclass-Codes/CC_Kubernetes/S9  kubectl get pods
NAME          READY   STATUS             RESTARTS   AGE
cmd-pod       0/1     Completed          1          12s
```

```yaml
er046256@w1738944  ~/tmp/Container-Masterclass-Codes/CC_Kubernetes/S9  kubectl describe pod cmd-pod
Name:         cmd-pod
Namespace:    default
Priority:     0
Node:         docker-desktop/192.168.65.3
Start Time:   Sat, 09 Jan 2021 16:45:20 -0600
Labels:       purpose=demonstrate-command
Annotations:  <none>
Status:       Running
IP:           10.1.0.10
IPs:
  IP:  10.1.0.10
Containers:
  cmd-container:
    Container ID:  docker://6e6b3a857a0840c560454be7ab3843d50756fe745945fdbc583cd71c46fb8392
    Image:         debian
    Image ID:      docker-pullable://debian@sha256:22d4552b9f96fd0ea943cb846d58b069d4df297673636055a3d984b3ccac6a28
    Port:          <none>
    Host Port:     <none>
    Command:
      printenv
    Args:
      HOSTNAME
      KUBERNETES_PORT
    State:          Waiting
      Reason:       CrashLoopBackOff
    Last State:     Terminated
      Reason:       Completed
      Exit Code:    0
      Started:      Sat, 09 Jan 2021 16:46:18 -0600
      Finished:     Sat, 09 Jan 2021 16:46:18 -0600
    Ready:          False
    Restart Count:  3
    Environment:    <none>
    Mounts:
      /var/run/secrets/kubernetes.io/serviceaccount from default-token-q4hf6 (ro)
Conditions:
  Type              Status
  Initialized       True
  Ready             False
  ContainersReady   False
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
  Type     Reason     Age                From               Message
  ----     ------     ----               ----               -------
  Normal   Scheduled  84s                default-scheduler  Successfully assigned default/cmd-pod to docker-desktop
  Normal   Pulled     75s                kubelet            Successfully pulled image "debian" in 7.8822339s
  Normal   Pulled     73s                kubelet            Successfully pulled image "debian" in 1.2677427s
  Normal   Pulled     55s                kubelet            Successfully pulled image "debian" in 1.220788s
  Normal   Pulling    27s (x4 over 83s)  kubelet            Pulling image "debian"
  Normal   Created    26s (x4 over 75s)  kubelet            Created container cmd-container
  Normal   Pulled     26s                kubelet            Successfully pulled image "debian" in 1.2130714s
  Normal   Started    25s (x4 over 75s)  kubelet            Started container cmd-container
  Warning  BackOff    13s (x6 over 72s)  kubelet            Back-off restarting failed container
```

```yaml
 ✘ er046256@w1738944  ~/tmp/Container-Masterclass-Codes/CC_Kubernetes/S9  kubectl logs cmd-pod
cmd-pod
tcp://10.96.0.1:443
```

