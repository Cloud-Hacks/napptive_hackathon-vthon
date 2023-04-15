# Jenkins

> Jenkins is a self-contained, open source automation server which can be used to automate all sorts of tasks related to building, testing, and delivering or deploying software.

Deploys a Jenkins client that can be accessed using the `jenkins:8080` endpoint. 
You can connect to the it from other applications or components running in the same environment.

# Usage

After deploying the application, you can find it in your terminal:

```
$ playground apps info jenkins
  NAME         STATUS
  jenkins      RUNNING

  COMPONENT     STATUS     SCOPES    TRAITS
  jenkins       RUNNING              napptive-ingress, storage

  COMPONENT     INGRESSES
  jenkins       jenks-client-<your-namespace>.apps.playground.napptive.dev

```

# How to access to Jenkins UI

After that check the logs until you get the password and it shows `Jenkins is fully up and running` 
Then open the public endpoint navigating through the web UI to select the application clicking on the associated Endpoint. 
To get the password, you need to find it from the logs or use `kubectl logs jenkins-<your-pod> | grep password -A3` .

