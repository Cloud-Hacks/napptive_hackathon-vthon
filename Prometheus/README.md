# Promotheus

> Prometheus is a systems and service monitoring system. It collects metrics from configured targets at given intervals, evaluates rule expressions, displays the results, and can trigger alerts if some condition is observed to be true.

Deploys a Prom server that can be accessed using the `prometheus:9090` endpoint. 
You can connect to the server from other applications or components running in the same environment.

# Usage

After deploying the application, you can find it in your terminal:

```
$ playground apps info prometheus
  NAME         STATUS
  prometheus    RUNNING

  COMPONENT     STATUS     SCOPES    TRAITS
  prometheus    RUNNING              napptive-ingress

  COMPONENT     INGRESSES
  prometheus    prom-server-<your-namespace>.apps.playground.napptive.dev

```

# How to access to Prometheus UI

After that open the public endpoint navigating through the web UI to select the application, selecting the Prom component, and clicking on the associated Endpoint. 
To provide your own configuration, you need to add your endpoints to be scraped in the prometheus.yml.
