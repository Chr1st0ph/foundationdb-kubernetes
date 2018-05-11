## work-in-progress: FoundationDB running on Kubernetes


A very basic Kubernetes statefulset running a FoundationDB cluster.

###configuration

##### Environment variables

* FDB\_DATACENTER\_ID : set datacenter_id
* FDB\_MACHINE\_ID : set machine_id ( defaults to spec.nodeName )

### current limitations/issues:

1. this setup has no Persistent Volume (Claim) configured (yet) !
2. only one coordinator can be configured for startup

This setup is tested on Minikube v0.25.0, Kubernetes client 1.9.3, Kubernetes server 1.9.0
  