# ArangoDB

> ArangoDB is a multi-model, open-source database with flexible data models for documents, graphs, and key-values. Build high performance applications using a convenient SQL-like query language or JavaScript extensions.

Deploys a Arango db server that can be accessed using the `arangodb:8529` endpoint. 
You can connect to the Arango db server from other applications or components running in the same environment.

# Usage

After deploying the application, you can use it in a local environment:

```
$ playground apps info arangodb
  NAME         STATUS
  arangodb     RUNNING

$ kubectl get svc arangodb
  NAME        TYPE        CLUSTER-IP      EXTERNAL-IP   PORT(S)    AGE
  arangodb    ClusterIP   10.120.5.45     <none>        8529/TCP   6h17m

```

For debugging and development you might want to access the ArangoDB workload directly. For example, if you created the deployment with name `arangodb`, you can forward the ArangoDB port from the pod as follows:

```shell
kubectl port-forward svc/arangodb 8529:8529
```
