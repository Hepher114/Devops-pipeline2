# Install Terraform on Ubuntu EC2
## Installation Steps
Following official Kubernetes documentation:  
[Official Terraform Installation Guide](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli)
---
<img width="1425" alt="Screen Shot 2025-05-29 at 8 41 38 PM" src="https://github.com/user-attachments/assets/ee57150a-3c28-4875-81fb-ed7ec09f8911" />

### Add HashiCorp Repos

```bash
sudo apt-get update && sudo apt-get install -y gnupg software-properties-common

wget -O- https://apt.releases.hashicorp.com/gpg | \
gpg --dearmor | \
sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg > /dev/null

echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] \
https://apt.releases.hashicorp.com $(lsb_release -cs) main" | \
sudo tee /etc/apt/sources.list.d/hashicorp.list

sudo apt update
### Install Terraform

```bash
sudo apt-get install terraform

### Verify Terraform Installation
```bash
terraform -help
