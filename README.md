# my-app
This is a Helm chart for deploying a frontend and backend application into a Kubernetes cluster and configuring ingress to access the application.

### Prerequisites
- A running Kubernetes cluster
- [Helm](https://helm.sh/) installed and configured in the cluster

### Usage
To install the chart:
```
helm install my-app .
```
To uninstall the chart:
```
helm uninstall my-app
```

### Configuration 
The following table lists the configurable parameters of the my-app chart and their default values.

|  Parameter	|  Description	|  Default  |
|-------------|---------------|-----------|
| `frontend.image` |	Frontend container image |	`my-registry/frontend:latest` |
| `frontend.replicas`	| Number of frontend replicas |	`1`
| `frontend.resources`	| Frontend container resource requests and limits |	`requests: memory: "64Mi", cpu: "250m", limits: memory: "128Mi", cpu: "500m"` |
|`backend.image`	| Backend container image	| `my-registry/backend:latest` |
| `backend.replicas` |	Number of backend replicas |	`2` |
| `backend.resources` |	Backend container resource requests and limits	| `requests: memory: "128Mi", cpu: "500m", limits: memory: "256Mi", cpu: "1"` |
| `ingress.enabled` |	Enable or disable ingress resource |	`true`
| `ingress.host`	| Hostname for the ingress resource |	`my-app.example.com` |
