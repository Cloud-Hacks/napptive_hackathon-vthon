# Timescaledb

> Timescaledb is an open-source time-series database optimized for fast ingest and complex queries. Engineered up from PostgreSQL, packaged as an extension.

Deploys a Timescale db server that can be accessed using the `timescaledb:5432` endpoint. 
You can connect to the Timescale db server from other applications or components running in the same environment.

# Usage

After deploying the application, you can use it in a local environment:

```
$ playground apps info timescaledb
  NAME         STATUS
  timescaledb  RUNNING

$ kubectl get svc timescaledb
  NAME        TYPE        CLUSTER-IP      EXTERNAL-IP   PORT(S)    AGE
  timescaledb ClusterIP   10.120.5.45     <none>        5432/TCP   6h17m

```
For debugging and development you might want to access the Timescaledb workload directly. For example, if you created the deployment with name `timescaledb`, you can forward the Timescaledb port from the pod as follows:

```shell
kubectl port-forward svc/timescaledb 5432:5432
```

You can access the container directly from locally installed PostgreSQL client tools such as psql. You have to set up the TimescaleDB [extension](https://docs.timescale.com/self-hosted/latest/install/installation-docker/#set-up-the-timescaledb-extension).

```
psql -U postgres -h localhost
```
