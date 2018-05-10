### work-in-progress: FoundationDB running on Kubernetes


A very basic Kubernetes statefulset running a FoundationDB cluster.

##### current limitations/issues:

1. this setup has no Persistent Volume (Claim) configured (yet) !
2. machine_id is not set in foundationdb.conf ( yet )
3. only one coordinator can be configured for startup

This setup is tested on Minikube v0.25.0, Kubernetes client 1.9.3, Kubernetes server 1.9.0
  