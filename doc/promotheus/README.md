# Prometheus 

Prometheus is a time-series database that collects and stores metrics from applications, services, and infrastructure. It is commonly used in cloud-native environments like Kubernetes.


## How it will work 
- Scrapes metrics from exporters (e.g., Node Exporter, cAdvisor, application endpoints).
- Stores data in its time-series database (TSDB).
- Uses PromQL to analyze and filter metrics.
- Sends alerts via Alertmanager based on defined rules.
- Integrates with Grafana for dashboards and visualization.


Difference between prometheus and metrics server 

![alt text](image.png)



## Kube prometheus stack 


````
helm upgrade --install kube-prometheus-stack prometheus-community/kube-prometheus-stack -f custom-values.yaml
````