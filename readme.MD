# K8s HPA

***install metric server for monitoring and autoscaling pods in a Kubernetes cluster. It collects resource usage metrics like CPU and memory consumption from the cluster's nodes and pods and provides them to Kubernetes for use in autoscaling, alerting, and monitoring***

**To enable Horizontal Pod Autoscaling (HPA) in Kubernetes, follow these steps:**

* **Install the Metrics Server:** This component collects CPU and memory usage data, which HPA uses to make scaling decisions.
* **Configure Resource Requests and Limits:** In our deployment's manifest file, define resource requests and limits for each container. This helps HPA understand the resources needed to maintain optimal performance.
* **Create an HPA Resource:** Define an HPA configuration in a manifest file to specify the target deployment, scaling metrics, and desired thresholds for autoscaling.


```
kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml
```

* deploy expense mysql, backend, frontend by adding resouces

```
kubectl top pods
```

this gives metrics like cpu and memory utilization of each pod

* install k9s. it provides a terminal UI to interact with your Kubernetes clusters

```
curl -sS https://webinstall.dev/k9s | bash
```

