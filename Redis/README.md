# Redis

> Redis is an open-source, in-memory data structure store, used as a database, cache, and message broker. It supports a wide range of data structures, including strings, hashes, lists, sets, and sorted sets. Redis provides high performance and scalability, making it a popular choice for use cases such as real-time analytics, caching, and message queueing.

Deploys a Redis server that can be accessed using the `redis:6379` endpoint. 
You can connect to the Redis server from other applications or components running in the same environment.

# Usage

After deploying the application, you can use it in a local environment:

```
$ playground apps info redis
  NAME         STATUS
  redis        RUNNING

$ kubectl get svc redis
  NAME        TYPE        CLUSTER-IP      EXTERNAL-IP   PORT(S)    AGE
  redis       ClusterIP   10.120.5.45     <none>        6379/TCP   6h17m

```
For debugging and development you might want to access the Redis workload directly. For example, if you created the deployment with name redis, you can forward the Redis port from the pod (e.g. redis-cd7c6bcd5-2p2v4) as follows:

```shell
kubectl port-forward redis-cd7c6bcd5-2p2v4 6379:6379
```
