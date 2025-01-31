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

````


