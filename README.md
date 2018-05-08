### work-in-progress: FoundationDB running on Kubernetes


A very basic Kubernetes statefulset running a FoundationDB cluster.

##### current issues:

1. this setup has no Persistent Volume (Claim) configured (yet) !
2. every pod runs two FoundationDB processes because not all processes are visible in cluster. This seems to be related to [https://forums.foundationdb.org/t/how-are-contributing-workers-computed/360/12](https://forums.foundationdb.org/t/how-are-contributing-workers-computed/360/12)
3. machine_id is not set in foundationdb.conf ( yet )
4. supports only one configured coordinator ( can be adapted on running cluster using fdbcli --exec "coordinators IP:4500")
5. down-scale ( without excluding servers beforehand )
6. occasionally "The database is available, but has issues (type 'status' for more information)." >> still not sure what is the problem

This setup is tested on Minikube v0.25.0, Kubernetes client 1.9.3, Kubernetes server 1.9.0
  