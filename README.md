# 🐳 Docker Cheat Sheet

Welcome to the Docker Cheat Sheet! This guide is designed to help beginners and intermediate users quickly reference essential Docker commands and concepts. Whether you're just starting out or need a refresher, this cheat sheet has got you covered.

---

## 📦 Table of Contents

1. [Installation](#installation)
2. [Docker Basics](#docker-basics)
3. [Image Management](#image-management)
4. [Container Management](#container-management)
5. [Networking](#networking)
6. [Volumes](#volumes)
7. [Docker Compose](#docker-compose)
8. [Dockerfile Instructions](#dockerfile-instructions)
9. [System Cleanup](#system-cleanup)
10. [Docker Swarm (Advanced)](#docker-swarm-advanced)
11. [Additional Resources](#additional-resources)

---

## Installation

### Ubuntu/Debian

```bash
sudo apt update
sudo apt install docker.io
```

### Arch Linux

```bash
sudo pacman -S docker
```

### Fedora

```bash
sudo dnf -y install dnf-plugins-core
sudo dnf config-manager --add-repo https://download.docker.com/linux/fedora/docker-ce.repo
sudo dnf install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

### Post-Installation Steps

```bash
sudo systemctl start docker
sudo systemctl enable docker
sudo docker run hello-world
```

---

## Docker Basics

```bash
docker --version       # Check Docker version
docker info            # Display system-wide information
docker help            # List all Docker commands
```

---

## Image Management

```bash
docker search <image>           # Search for an image
docker pull <image>             # Pull an image
docker images                   # List images
docker rmi <image>              # Remove image
docker build -t <name> .        # Build image from Dockerfile
```

---

## Container Management

```bash
docker run -it <image>                  # Run a container interactively
docker run -d <image>                   # Run a container in detached mode
docker ps                               # List running containers
docker ps -a                            # List all containers
docker stop <container>                # Stop container
docker start <container>               # Start container
docker rm <container>                  # Remove container
docker exec -it <container> bash       # Shell access to container
docker logs <container>                # View logs
```

---

## Networking

```bash
docker network ls                               # List networks
docker network create <network>                 # Create network
docker network connect <network> <container>    # Connect container
docker network disconnect <network> <container> # Disconnect container
```

---

## Volumes

```bash
docker volume ls                     # List volumes
docker volume create <name>         # Create volume
docker volume inspect <name>        # Inspect volume
docker volume rm <name>             # Remove volume
docker run -v <name>:/path <image>  # Use volume in container
```

---

## Docker Compose

```bash
docker-compose up              # Start services
docker-compose up -d          # Detached mode
docker-compose down           # Stop services
docker-compose build          # Build/rebuild services
docker-compose logs           # View logs
```

---

## Dockerfile Instructions

- `FROM`: Base image
- `RUN`: Execute commands during build
- `CMD`: Default command for container
- `LABEL`: Metadata
- `EXPOSE`: Port to expose
- `ENV`: Environment variables
- `ADD`: Copy files with additional features
- `COPY`: Copy files
- `ENTRYPOINT`: Run container as executable
- `VOLUME`: Mount point
- `WORKDIR`: Working directory

---

## System Cleanup

```bash
docker container prune       # Remove stopped containers
docker image prune           # Remove unused images
docker network prune         # Remove unused networks
docker volume prune          # Remove unused volumes
docker system prune          # Remove all unused data
```

---

## Docker Swarm (Advanced)

```bash
docker swarm init                                 # Initialize swarm
docker swarm join --token <token> <ip>:<port>     # Join swarm
docker node ls                                    # List swarm nodes
docker stack deploy -c <file> <stack>             # Deploy stack
docker stack services <stack>                     # List services
docker stack rm <stack>                           # Remove stack
```

---

## Additional Resources

- [Docker Documentation](https://docs.docker.com/)
- [Docker Hub](https://hub.docker.com/)
- [Docker CLI PDF Cheat Sheet](https://docs.docker.com/get-started/docker_cheatsheet.pdf)

---

💡 **Contributions are welcome!** Feel free to open a pull request if you have additional commands, tips, or corrections.


 
  
