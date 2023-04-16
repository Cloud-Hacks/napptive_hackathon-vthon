# percona

> percona Server for MySQL is a free, fully compatible, enhanced, open source drop-in replacement for MySQL.

Deploys a percona server that can be accessed using the `percona:8080` endpoint. 
You can connect to the percona server from other applications or components running in the same environment.

# Usage

After deploying the application, you can use it in a local environment:

```
$ playground apps info percona
  NAME         STATUS
  percona      RUNNING

$ kubectl get svc percona
  NAME        TYPE        CLUSTER-IP      EXTERNAL-IP   PORT(S)    AGE
  percona     ClusterIP   10.120.5.45     <none>        8080/TCP   6h17m

```

For debugging and development you might want to access the percona workload directly. For example, if you created the deployment with name `percona`, you can forward the percona port from the pod as follows:

```shell
kubectl port-forward svc/percona 8080:8080
```
