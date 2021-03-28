# Cluster IP a224ecb94822476f9f70a16ad77baa69

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: deploy-nginx
spec:
  selector:
    matchLabels:
      run: my-nginx
  replicas: 2
  template:
    metadata:
      labels:
        run: my-nginx
    spec:
      containers:
      - name: deploy-container
        image: nginx
        ports:
        - containerPort: 80
```

```yaml
apiVersion: v1
kind: Service
metadata:
  name: serve-nginx
  labels:
    run: my-nginx
spec:
  ports:
  - port: 80
    protocol: TCP
  selector:
    run: my-nginx
```

* `port`
  * TCP 80 is supposed to be exposed using this service
* `selector`
  * determines which pods to expose

    ```yaml
    er046256@w1738944  ~/tmp/Container-Masterclass-Codes/CC_Kubernetes/S11/ClusterIP service  kgp
    NAME                            READY   STATUS    RESTARTS   AGE
    deploy-nginx-54b8848497-7rbzs   1/1     Running   0          16s
    deploy-nginx-54b8848497-rlvkv   1/1     Running   0          16s
    er046256@w1738944  ~/tmp/Container-Masterclass-Codes/CC_Kubernetes/S11/ClusterIP service  kubectl get svc
    NAME          TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)   AGE
    kubernetes    ClusterIP   10.96.0.1        <none>        443/TCP   87m
    serve-nginx   ClusterIP   10.109.105.123   <none>        80/TCP    65s
    ```

```yaml
er046256@w1738944  ~/tmp/Container-Masterclass-Codes/CC_Kubernetes/S11/ClusterIP service  kubectl describe svc serve-nginx
Name:              serve-nginx
Namespace:         default
Labels:            run=my-nginx
Annotations:       <none>
Selector:          run=my-nginx
Type:              ClusterIP
IP:                10.106.161.73
Port:              <unset>  80/TCP
TargetPort:        80/TCP
Endpoints:         10.1.0.21:80,10.1.0.22:80
Session Affinity:  None
Events:            <none>
```

