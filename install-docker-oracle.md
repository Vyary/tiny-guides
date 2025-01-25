# Install Docker on Oracle Linux 8 (ARM-based VPS)

## 1. Update the System
Run the following commands to ensure your system is up-to-date:
```bash
sudo dnf update -y
```
```bash
sudo dnf install -y yum-utils
```

## 2. Add the Docker Repository
Add the Docker CE repository for Oracle Linux:
```bash
sudo dnf config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
```
Oracle Linux uses the same repository as CentOS for Docker.

## 3. Install Docker
Install Docker and its dependencies:
```bash
sudo dnf install -y docker-ce docker-ce-cli containerd.io
```

## 4. Enable and Start the Docker Service
Enable Docker to start at boot and start the service:
```bash
sudo systemctl enable docker
```
```bash
sudo systemctl start docker
```

## 5. Verify Docker Installation
Check the Docker version and ensure it is running:
```bash
docker --version
```
```bash
sudo systemctl status docker
```

## 6. (Optional) Add Your User to the Docker Group
To run Docker commands without `sudo`, add your user to the Docker group:
```bash
sudo usermod -aG docker $USER
```
Log out and back in for the group change to take effect.

## 7. Test Docker
Run a test container to confirm Docker is working correctly:
```bash
docker run hello-world
```
