# NodePort 35e17e3aebe04e4d89e8f5badd97bc14

ClusterIP : Exposes the Service on a cluster-internal IP. Choosing this value makes the Service only reachable from within the cluster. This is the default ServiceType . NodePort : Exposes the Service on each Node's IP at a static port \(the NodePort \).

```yaml
apiVersion: v1
kind: Service
metadata:
  name: serve-nginx
  labels:
    run: my-nginx
  type: NodePort
  ports:
  - port: 8080
    targetPort: 80
    protocol: TCP
    name: http
  - port: 443
    protocol: TCP
    name: https
  selector:
    run: my-nginx
```

* `NodePort`
* same selector

