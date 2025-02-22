# Docker Cheat Sheet

## General Commands
- **Check Docker version**  
  `docker --version`

- **Check system-wide information about Docker**  
  `docker info`

- **Run a simple container**  
  `docker run hello-world`

## Managing Images
- **List all downloaded images**  
  `docker images`

- **Search for an image in Docker Hub**  
  `docker search nginx`

- **Download an image from Docker Hub**  
  `docker pull nginx`

- **Remove an image**  
  `docker rmi image_id`

- **Build an image from a Dockerfile**  
  `docker build -t my-image .`

- **Tag an image**  
  `docker tag my-image myrepo/my-image:v1`

- **Push an image to Docker Hub**  
  `docker push myrepo/my-image:v1`

## Managing Containers
- **List running containers**  
  `docker ps`

- **List all containers (including stopped ones)**  
  `docker ps -a`

- **Start a container**  
  `docker start container_id`

- **Stop a container**  
  `docker stop container_id`

- **Restart a container**  
  `docker restart container_id`

- **Remove a container**  
  `docker rm container_id`

- **Remove all stopped containers**  
  `docker container prune`

- **Run an interactive container**  
  `docker run -it ubuntu bash`

- **Run a detached container**  
  `docker run -d nginx`

- **Run a container with a specific name**  
  `docker run --name my-container nginx`

- **Run a container and publish a port**  
  `docker run -p 8080:80 nginx`

- **Run a container and mount a volume**  
  `docker run -v /host/path:/container/path nginx`

## Container Logs & Inspection
- **View logs of a running container**  
  `docker logs container_id`

- **Follow logs in real-time**  
  `docker logs -f container_id`

- **Inspect a container's details**  
  `docker inspect container_id`

- **View running processes inside a container**  
  `docker top container_id`

- **Access a running container's shell**  
  `docker exec -it container_id bash`

## Managing Volumes
- **List all volumes**  
  `docker volume ls`

- **Create a volume**  
  `docker volume create my_volume`

- **Remove a volume**  
  `docker volume rm my_volume`

- **Remove all unused volumes**  
  `docker volume prune`

## Managing Networks
- **List all networks**  
  `docker network ls`

- **Create a new network**  
  `docker network create my_network`

- **Connect a container to a network**  
  `docker network connect my_network container_id`

- **Disconnect a container from a network**  
  `docker network disconnect my_network container_id`

- **Remove a network**  
  `docker network rm my_network`

- **Remove all unused networks**  
  `docker network prune`

## Docker Compose
- **Start services defined in a `docker-compose.yml` file**  
  `docker-compose up -d`

- **Stop services**  
  `docker-compose down`

- **Restart services**  
  `docker-compose restart`

- **View logs from services**  
  `docker-compose logs`

- **View running services**  
  `docker-compose ps`

## Cleaning Up
- **Remove all stopped containers**  
  `docker container prune`

- **Remove all unused images**  
  `docker image prune`

- **Remove all unused networks**  
  `docker network prune`

- **Remove all unused volumes**  
  `docker volume prune`

- **Remove everything (containers, images, networks, and volumes)**  
  `docker system prune -a`

## Other Useful Commands
- **Run a temporary container and remove it after exit**  
  `docker run --rm ubuntu bash`

- **Copy files from container to host**  
  `docker cp container_id:/path/to/file /host/path`

- **Copy files from host to container**  
  `docker cp /host/path container_id:/path/to/file`

- **View disk usage of Docker objects**  
  `docker system df`

- **Save an image as a tar archive**  
  `docker save -o my_image.tar my_image`

- **Load an image from a tar archive**  
  `docker load -i my_image.tar`

- **Show real-time resource usage statistics of containers**  
  `docker stats`

