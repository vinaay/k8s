# Splunk 


## Installation 

### Add Splunk Helm Repository
````
helm repo add splunk https://splunk.github.io/splunk-helm-chart
helm repo update
````




### Install Splunk
````
helm install splunk splunk/splunk \
  --set splunk.image.repository=docker.io/splunk/splunk \
  --set splunk.image.tag=latest \
  --set splunk.password=Splunk@123 \
  --set persistence.storageClass=standard
````

### Access splunk UI 
````
kubectl port-forward svc/splunk 8000:8000
````

