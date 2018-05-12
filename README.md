## work-in-progress: FoundationDB running on Kubernetes


A very basic Kubernetes StatefulSet running a [FoundationDB](https://www.foundationdb.org) cluster.

You can start a StatefulSet, and scale it up and down ( keep fault-tolerance of your cluster in mind ).

Let me know about your experience, please.


### configuration

##### Environment variables

* FDB\_DATACENTER\_ID : set datacenter_id ( optional )
* FDB\_MACHINE\_ID : set machine_id ( optional, defaults to spec.nodeName ).
  
  Hint: If you want to test redundancy/coordinator changes on a single-node-environment ( e.g. Minikube ), then you need to disable this in [statefulset.yaml](https://github.com/Chr1st0ph/foundationdb-kubernetes/blob/master/yaml/statefulset.yaml).

### current limitations/issues:

1. this setup has no Persistent Volume (Claim) configured (yet) !
2. only one coordinator can be configured for startup

This setup is tested on Minikube v0.25.0, Kubernetes client 1.9.3, Kubernetes server 1.9.0
  