# Kubectl Installation on Ubuntu EC2

This guide provides a quick way to install `kubectl`, the Kubernetes command-line tool, on an Ubuntu EC2 instance. Kubectl allows you to run commands against Kubernetes clusters, deploy applications, inspect and manage cluster resources, and view logs.

## Installation Steps
Following official Kubernetes documentation:  
[https://kubernetes.io/docs/tasks/tools/install-kubectl-linux](https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/#install-kubectl-binary-with-curl-on-linux)
### Download kubectl
```
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
```

### Install Kubectl
```
sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
```

### Verify Kubectl
```
kubectl version --client
```
