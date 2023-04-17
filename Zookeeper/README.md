# Zookeeper

> ZooKeeper is a centralized service for maintaining configuration information, naming, providing distributed synchronization, and providing group services. All of these kinds of services are used in some form or another by distributed applications. Each time they are implemented there is a lot of work that goes into fixing the bugs and race conditions that are inevitable.

Deploys a Zookeeper server that can be accessed using the `zookeeper:2181` endpoint. 
You can connect to the Zookeeper server from other applications or components running in the same environment.

# Usage

After deploying the application, you can use it in a local environment:

```
$ playground apps info zookeeper
  NAME         STATUS
  zookeeper    RUNNING

$ kubectl get svc zookeeper
  NAME        TYPE        CLUSTER-IP      EXTERNAL-IP   PORT(S)    AGE
  zookeeper   ClusterIP   10.120.5.45     <none>        2181/TCP   6h17m

```

For debugging and development you might want to access the Zookeeper cluster directly. For example, if you created the deployment with name zookeeper, you can forward the Zookeeper port from the pod (e.g. zookeeper-0) as follows and test the commands from [here](https://zookeeper.apache.org/doc/r3.8.1/zookeeperCLI.html) :

```shell
kubectl port-forward zookeeper-0 2181:2181
```
