# Helm charts

Helm charts are a powerful way to manage Kubernetes applications. A Helm chart is a collection of YAML files that define a set of Kubernetes resources, such as deployments, services, and config maps, which make up an application or service.


## Helm commands 

- helm install <chart-name>: Installs a chart into the Kubernetes cluster.
- helm upgrade <release-name> <chart-name>: Upgrades an existing release.
- helm uninstall <release-name>: Removes a release from the cluster.
- helm list: Lists all installed Helm releases.
- helm search <chart-name>: Searches for available charts in a repository.



## Sample helm chart create 

````
helm create my-nginx

cd my-nginx

helm install my-nginx ./my-nginx


helm upgrade install my-nginx ./my-nginx

kubectl get pods

kubectl port-forward svc/my-nginx-nginx 8080:80

helm uninstall my-nginx

````
