# port forward 


command is used to forward one or more local ports to a port on a pod running in a Kubernetes cluster. This is particularly useful when you want to access a service or application running inside the cluster without exposing it externally.



````
kubectl port-forward pod/dep-nginx-8d86fbbdd-t2fwf 8002:8002

kubectl port-forward service/my-service 8080:80

````


## Common Use Cases 
- Debugging applications running inside the cluster.
- Accessing internal services without exposing them via an external load balancer or ingress.
- Testing APIs or web interfaces of deployed application