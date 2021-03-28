# Kubernetes Architecture 6334beafff3e4f34ad2588299d84e2b0

## Kubernetes Architecture

Master → Node

## Master

### runs a set of applications

* kube-apiserver
  * serves rest requests passed to it
* kube-controllermanager
* kube-scheduler
  * schedules pods
* etcd
  * can only communicate with kube-apiserver

## Node

### runs a set of components

* kubelet
  * The worker
* kube-proxy
  * manages node communication other nodes

if on a cloud platform

* kube-controllermanager would talk to kube-proxy over cloud connection

kubernetes tries to desired state matches cuurent state

* reconciliation loop

