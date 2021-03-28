# Operating Kubernetes 95ecacb34de64e10a9dd0199479f1d03

## Operating Kubernetes

object management

## Two ways to manage kubernetes

### imperative \(via commands or yaml files\)

* explicit
  * create
  * update
  * scale

### declaritive \(via files\)

* let K8s figure it out

#### imperative

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: imp-pod
  labels:
    app: myapp
spec:
  containers:
  - name: imp-container
    image: busybox
    command: ['sh', '-c', 'echo Welcome to Container Masterclass by CeruleanCanvas && sleep 60']
```

* `kind` Pod is the type of unit
* `metadata`
  * `name` name of the pod
  * `label`
* `spec` specifications = object configuration informatio
  * `containers` field of the parent object which is `Pod`
    * `name` different from the name of the pod
    * `image` describe the image that is going to used by this container
    * `command` run a shell command that echo's the command listed

```bash
kubectl create -f imperative-pod.yaml
```

#### declaritively

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: dec-pod
  labels:
    app: myapp
spec:
  containers:
  - name: dec-container
    image: busybox
    command: ['sh', '-c', 'echo Welcome to the Container MasterClass by CeruleanCanvas && sleep 120']
```

```bash
kubectl apply -f declaritive-pod.yaml
```

```bash
kubectl get pods
```

```bash
kubectl describe pods imp-pod
kubectl describe pods dec-pod
```

