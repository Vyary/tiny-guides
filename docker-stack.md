# Deploy with Docker Stack to VPS

### 1. **Create SSH Keys**
Generate SSH keys to securely connect to your VPS.

### 2. **Give Read Permissions to the Private Key**
Ensure the private key is properly protected with the correct permissions:
```bash
chmod 400 <ssh-key>
```

### 3. **Try Connecting to the VPS**
Use the following command to connect to your VPS via SSH:
```bash
ssh -i <ssh-key.key> username@public-ip
```

### 4. **Install Docker on the VPS**
Follow the [official Docker installation guide](https://docs.docker.com/get-docker/) for your VPS's operating system.

### 5. **Initiate Docker Swarm**
Initialize Docker Swarm on your VPS to enable clustering:
```bash
docker swarm init
```

### 6. **Add Secrets to Docker on the VPS (Optional)**
Store sensitive data (such as passwords) as Docker secrets:
```bash
echo "mysecretvalue" | docker secret create <my_secret> -
```

### 7. **Create Docker Context for Easy Navigation (Optional)**
Create a Docker context to make it easier to manage remote Docker instances:
```bash
docker context create <context-name> --docker "host=ssh://username@public-ip"
```

### 8. **Switch to Docker Context (If Applicable)**
Switch to the Docker context you created for easier management:
```bash
docker context use <context-name>
```

### 9. **Start SSH Agent**
Start the SSH agent to manage your SSH keys:
```bash
eval "$(ssh-agent -s)"
```

### 10. **Add VPS Private Key to SSH Agent**
Add your private key to the SSH agent:
```bash
ssh-add <ssh-key.key>
```

### 11. **Deploy to VPS with Docker Stack**
Deploy your Docker stack to the VPS using your `docker-compose.yaml` file:
```bash
docker stack deploy -c docker-compose.yaml <stack-name>
```
