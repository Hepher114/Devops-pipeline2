# Kubectl Installation on Ubuntu EC2

This guide provides the quickest way to install `kubectl`, the Kubernetes command-line tool, on an Ubuntu EC2 instance. Kubectl allows you to run commands against Kubernetes clusters, deploy applications, inspect and manage cluster resources, and view logs.

## Installation Steps
Following official Kubernetes documentation:  
[https://kubernetes.io/docs/tasks/tools/install-kubectl-linux](https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/#install-kubectl-binary-with-curl-on-linux)

```bash
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
```

```bash
sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
```

Test to ensure the version you installed is up-to-date:
```bash
kubectl version --client
