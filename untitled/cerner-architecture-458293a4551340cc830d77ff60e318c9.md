# Cerner Architecture 458293a4551340cc830d77ff60e318c9

## Cerner Architecture

[Kube Dashboard Shots](Kubernetes%20and%20Docker%20-%20The%20Container%20Masterclass%20c0d50b427db0483ba561d344502dbb1e/Cerner%20Architecture%20458293a4551340cc830d77ff60e318c9/Kube%20Dashboard%20Shots%20b33a54ed6ff4442984182cf14cd41b93.md)

## Terms[¶](https://pages.github.cerner.com/norbert/kubernetes_operations/terms/#terms)

### DCOS to Kubernetes Terms[¶](https://pages.github.cerner.com/norbert/kubernetes_operations/terms/#dcos-to-kubernetes-terms)

[Untitled](Kubernetes%20and%20Docker%20-%20The%20Container%20Masterclass%20c0d50b427db0483ba561d344502dbb1e/Cerner%20Architecture%20458293a4551340cc830d77ff60e318c9/Untitled%20Database%2079c70bf6379c4b9eb532d43e55480f40.csv)

### Alva Services[¶](https://pages.github.cerner.com/norbert/kubernetes_operations/terms/#alva-services)

This section includes examples from Alva to help relate terms.

A single Alva Service `ml-relationship` is built into a container.

The Alva `ml-relationship` Container is put into a [Pod](https://kubernetes.io/docs/concepts/workloads/pods/pod/). A [Pod](https://kubernetes.io/docs/concepts/workloads/pods/pod/) is the smallest and simplest kubernetes object. It represents a set of running containers on the cluster. This set of containers for the Alva [Pod](https://kubernetes.io/docs/concepts/workloads/pods/pod/) are, the Alva `ml-relationship` Container, a Splunk Forwarder `fluentd`, and a Service Mesh Proxy `envoy`.

A single [Pod](https://kubernetes.io/docs/concepts/workloads/pods/pod/) and all of the containers grouped in that [Pod](https://kubernetes.io/docs/concepts/workloads/pods/pod/) are deployed to a single Kubernetes Agent.

Multiple Alva `ml-relationship` [Pod's](https://kubernetes.io/docs/concepts/workloads/pods/pod/) are grouped into a [ReplicaSet](https://kubernetes.io/docs/concepts/workloads/controllers/replicaset/). A [ReplicaSet](https://kubernetes.io/docs/concepts/workloads/controllers/replicaset/) ensures that a specified number of pods replicas are running at one time. There would be two Alva `ml-relationship` [Pod's](https://kubernetes.io/docs/concepts/workloads/pods/pod/) in a [ReplicaSet](https://kubernetes.io/docs/concepts/workloads/controllers/replicaset/).

Alva `ml-relationship` [ReplicaSet's](https://kubernetes.io/docs/concepts/workloads/controllers/replicaset/) are created from a [Deployment](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/). You describe a desired state in a [Deployment](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/) object, and the Deployment controller changes the actual state to the desired state at a controlled rate. Today there would be a [Deployment](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/) per Client per Domain per Service.

When updating the [Deployment](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/) for a new version of a Alva `ml-relationship` Container, Kubernetes will create a new [ReplicaSet](https://kubernetes.io/docs/concepts/workloads/controllers/replicaset/) and rolling deploy out the new version.

[Untitled](Kubernetes%20and%20Docker%20-%20The%20Container%20Masterclass%20c0d50b427db0483ba561d344502dbb1e/Cerner%20Architecture%20458293a4551340cc830d77ff60e318c9/Untitled%20Database%200e368fbc10ce4d4ebc32b62357fd69e8.csv)

