##### Why Kubernetes - GCLOUD?
   Kubernetes lets you deploy containers on a cluster(_set of nodes(instances)_). It is able to load balance traffic to containers and distribute the network traffic so that the deployment is stable.

* __How Does Kubernetes do it ?__
   For a stable deployment, kubernetes first creates a service w/ a fixed IP Addr for your pods.
   > A service is the fundamental way Kubernetes represents load balancer(Network LB w/ public IP). It groups set of pods together and provides a stable endpoint for them.

   By default pods in your deployment are only accessible in your cluster so to allow access over the internet, connect a load balancer and then kubernetes will create the service:
   > `$ kubectl expose deployments nginx --port=port --type=loadbalancer`
   
   * To get service: `$ kubectl get services`
   _Any client that hits the service externalIP will be routed to the pods behind the service._

* __Why do you need a service for a stable IP?__
   Since deployment create and destroy pods, the internal pods may not be stable so a service to a stable ip is a better way to manage connections.

* __Extra Notes__:
   * Use declarative cmds like `config files` to scale your deployments so you can update anytime and apply the new changes.
   * To avoid downtime while your app redeploys, use an update strategy (_eg. RollingUpdate_).
   * To view replicas: `$ kubectl get replicasets`
   * To see active pods `$ kubectl get pods`
   * To check deployments: `$ kubectl get deployments`


