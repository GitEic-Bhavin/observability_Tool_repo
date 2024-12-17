##### What are kube-state-metrics?
- kube-state-metrics listens to the Kubernetes API server and generates metrics about Kubernetes object states. It provides a metrics endpoint for Prometheus, offering insights into the health and status of various resources.

##### What is the difference between node exporter and kube-state-metrics?
- Node exporter collects system-level metrics from nodes (CPU, memory, disk usage), while kube-state-metrics generates metrics about Kubernetes objects (pods, deployments, services). They work together to give a complete view of cluster health.

##### What metrics are provided by kube-state-metrics in Kubernetes?
- kube-state-metrics provides metrics such as pod status, deployment status, node capacity, PersistentVolume and PersistentVolumeClaim status, and service details.

##### How do I monitor pod status using kube-state-metrics in Kubernetes?
- Use Prometheus queries like
```
kube_pod_status_phase{phase="Running"} for running pods and kube_pod_container_status_restarts_total for container restart counts.
```

###### node-exporter will fetch all info about each node and push to prometheus server. prometheus server will store that scraped data into Time Series DB.
###### Thatsfor node-exporter will run as deamon-set.
###### kube-state-metrics will talk to kube API  server by api call for get info about kube status. like pods, deployments, replicaset, services etc.

- If you want to go inside node-exporter pods.
- just ssh into minikube / eks cluster via ssh into ec2 instance / aks same with ssh.

- for minikube
```
minikube ssh
# send curl request to node-exporter pods
curl cluster_ip:9100/metrics
```

##### Run PromQL Qurey for
1. how many times pods restarted
- Go to Prometheus localhost:9090
```
kube_pod_container_status_restarts_total
```
2. Fetch kube status for defult namespace
```
kube_pod_container_status_restarts_total{namespace="default"}
```

3. how many times container init
```
kube_pod_init_container_status_restarts_total{namespace="eks-monitoring"}
```


##### Grafana the Visualization Tool
- You can Visualized your collected data into Time Series DB of Prometheus with Graph.
- In Additional, you may have control over your Dashboard of various Metrics for who can see your Dashboard using IAM.
- You may have authentications & authorizations also.