# Crashlookbackoff


## How to genetrate the load 

````
python3 -m venv locust && \
cd locust && \
source bin/activate && \
pip3 install -q locust && \
locust --version


````


Create file locust.py

````
from locust import HttpUser, task

class Test(HttpUser):
    @task
    def authenticate_task(self):
        self.client.get("/")
````



run below command to start generate the load 

````
locust 
````