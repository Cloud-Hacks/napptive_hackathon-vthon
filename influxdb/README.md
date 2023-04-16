# Influxdb

> InfluxDB is a time series database built from the ground up to handle high write and query loads.

Deploys a influx db server that can be accessed using the `Influxdb:8086` endpoint. 
You can connect to the influx db server from other applications or components running in the same environment.

# Usage

After deploying the application, you can use it in a local environment:

```
$ playground apps info Influxdb
  NAME         STATUS
  Influxdb     RUNNING

$ kubectl get svc Influxdb
  NAME        TYPE        CLUSTER-IP      EXTERNAL-IP   PORT(S)    AGE
  Influxdb    ClusterIP   10.120.5.45     <none>        8086/TCP   6h17m

```

For debugging and development you might want to access the Influxdb workload directly. For example, if you created the deployment with name `Influxdb`, you can forward the Influxdb port from the pod as follows:

```shell
kubectl port-forward svc/Influxdb 8086:8086
```
