# Pod Lifecycle f72443d1cc354d6a8bcc6ce83f1a2a13

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: lifecyc-pod
spec:
  containers:
  - name: lifecyc-container
    image: nginx
    lifecycle:
      postStart:
        exec:
          command: ["/bin/sh", "-c", "echo Welcome! > /usr/share/poststart-msg"]
      preStop:
        exec:
          command: ["/usr/sbin/nginx","-s","quit"]
```

`lifecycle`

* `postStart`
  * `command` run the command after it starts
* `preStop`
  * run this before it stops

```yaml
kubectl create -f lifycyc-pod.yaml.yaml
```

```yaml
kubectl describe pods lifycyc-pod
```

```yaml
kubectl exec -it lifecyc-pod -- /bin/bash
root@lifecyc-pod:/# cat /usr/share/poststart-msg
Welcome!
```

