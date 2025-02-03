# Basic commands


````
kubectl get namespace 

kubectl get pod -n namespace
kubectl get deployment -n namespace

kubectl get cm -n namespace 
kubectl get secrets -n namespace 


To troubleshoot the pod 
kubectl describe pod_name -n namespace 

kubectl logs -f pod_name -n namespace


To login terminal inside the cluset 
kubectl exec -it pod_name -n namesapce 

kubectl port-forward pod/dep-nginx-8d86fbbdd-t2fwf 8002:8002

kubectl port-forward service/my-service 8080:80

kubectl top node 

kubectl top pod

````


