# K8s HPA

***install metric server for monitoring and autoscaling pods in a Kubernetes cluster. It collects resource usage metrics like CPU and memory consumption from the cluster's nodes and pods and provides them to Kubernetes for use in autoscaling, alerting, and monitoring***



* install metric server
* configure `resources(request,limit)` for each pod in Deployment manifest file

```
kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml
```

* deploy expense mysql, backend, frontend

```
kubectl top pods
```

this gives metrics like cpu and memory utilization of each pod

* install k9s. it provides a terminal UI to interact with your Kubernetes clusters

```
curl -sS https://webinstall.dev/k9s | bash
```

