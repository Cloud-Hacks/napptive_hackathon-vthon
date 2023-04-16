# Cortex

> Cortex provides long term storage for Prometheus metrics, and allows you to query and visualize your metrics using Grafana.

Deploys a Prom server that can be accessed using the `coretex:9009` endpoint. 
You can connect to the server from other applications or components running in the same environment.

# Usage

After deploying the application, you can find it in your terminal:

```
$ playground apps info cortex
  NAME         STATUS
  cortex       RUNNING

  COMPONENT     STATUS     SCOPES    TRAITS
  cortex        RUNNING              napptive-ingress

  COMPONENT     INGRESSES
  cortex        cortex-client-<your-namespace>.apps.playground.napptive.dev

```

# How to access to Prometheus UI

The Cortex UI can be accessed using the cortex-ing:<port> endpoint. For example, if you expose the cortex-ing component on port 9009, you can access it using http://cortex-ing:<port>/ or http://<public-ip>:<port>/.
