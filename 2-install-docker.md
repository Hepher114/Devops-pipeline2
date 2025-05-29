# Docker Installation on Ubuntu EC2

This guide follows the [official Docker documentation](https://docs.docker.com/engine/install/ubuntu/) for installing Docker on an Ubuntu EC2 instance.

<img width="1413" alt="Screen Shot 2025-05-28 at 5 31 39 PM" src="https://github.com/user-attachments/assets/eaeebd03-6928-4239-9dd1-8ec7759deec2" />

## Complete Installation Commands

Run these commands sequentially to install Docker:

```bash
# Update package index and install prerequisites
sudo apt-get update
sudo apt-get install ca-certificates curl

# Add Docker's official GPG key
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the Docker repository
echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}") stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

# Update package index again
sudo apt-get update

# Install Docker packages
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

# Verify installation
sudo docker run hello-world
## Optional: Run Docker Without `sudo`

To allow the `ubuntu` user to run Docker commands without needing `sudo`, add the user to the Docker group:

```bash
sudo usermod -aG docker ubuntu
