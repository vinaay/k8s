# Install istio 

Download required software 
````
curl -L https://istio.io/downloadIstio | sh -
cd istio-*
export PATH=$PWD/bin:$PATH
````


Install Istio Base Chart
````
helm install istio-base manifests/charts/base -n istio-system

````

Install Istio Control Plane

````
helm install istiod manifests/charts/istio-control/istio-discovery -n istio-system

````

Install the Istio Ingress Gateway

````
helm install istio-ingress manifests/charts/gateways/istio-ingress -n istio-system

````

