# Install Kubernetes
There are multiple ways to install kubernetes on your local machine. You can choose any one of the following options. 
1. Via Docker Desktop
2. Minikube
3. Cloud Provider (You will need an account with the cloud provider)

> You don't need to set up all 3, just choose the one that is best for you.

## 1. Docker Desktop
1. From the Docker Dashboard, select the Settings.
2. Select Kubernetes from the left sidebar.
3. Next to Enable Kubernetes, select the checkbox.
4. Select Apply & Restart.

> By default, Kubernetes containers are hidden from commands like docker ps, because managing them manually is not supported. Most users do not need this option. To see these internal containers, select Show system containers (advanced).


## 2. Via Minikube
1. MacOS
```bash
brew install minikube kubectl

minikube start
```

2. Linux
```bash
# install minikube
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube
# install kubectl
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl

minikube start
```