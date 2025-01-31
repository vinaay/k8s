# Using calico 

Create a NetworkPolicy to control the communication between pods. Here’s a step-by-step guide to implementing a NetworkPolicy in Minikube:


````
minikube start --network-plugin=cni --cni=calico


minikube addons enable calico


kubectl apply -f test-deployment.yaml

kubectl expose deployment test-deployment --port=80 --target-port=80 --type=ClusterIP



kubectl create nginx --image=nginx -l access=allowed

````