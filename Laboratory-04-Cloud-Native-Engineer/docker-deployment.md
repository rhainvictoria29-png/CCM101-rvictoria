# Docker Deployment and Container Lifecycle

## Introduction

This document records the Docker commands I used to deploy and manage an Nginx web server in the KillerCoda Playground. The activity demonstrates how containers can be created, accessed, stopped, and removed using the Docker Command Line Interface.

## Checkpoint 3 – Docker Environment

### 1. Check Docker Version

```bash
docker --version
```

**Explanation:** This command displays the installed Docker version and confirms that Docker is available in the terminal.

### 2. Check Docker Information

```bash
docker info
```

**Explanation:** This command displays detailed information about the Docker environment, including the server configuration and running containers.

## Checkpoint 4 – Deploy Nginx

### 1. Pull the Nginx Image

```bash
docker pull nginx
```

**Explanation:** This command downloads the official Nginx image from Docker Hub so it can be used to create a container.

### 2. Run the Nginx Container

```bash
docker run -d --name my-nginx -p 8080:80 nginx
```

**Explanation:** This command creates and runs an Nginx container in detached mode and maps host port 8080 to container port 80.

### 3. Test the Web Server

```bash
curl http://localhost:8080
```

**Explanation:** This command sends an HTTP request to the Nginx web server and displays its HTML response in the terminal.

## Checkpoint 5 – Container Lifecycle

### 1. List Running Containers

```bash
docker ps
```

**Explanation:** This command lists all currently running Docker containers.

### 2. Stop the Container

```bash
docker stop my-nginx
```

**Explanation:** This command stops the running Nginx container named my-nginx.

### 3. Verify the Container Status

```bash
docker ps
```

**Explanation:** This command verifies that the Nginx container is no longer running.

### 4. Display All Containers

```bash
docker ps -a
```

**Explanation:** This command displays both running and stopped containers, allowing me to confirm that my-nginx has stopped.

### 5. Remove the Container

```bash
docker rm my-nginx
```

**Explanation:** This command permanently removes the stopped my-nginx container from the Docker environment.

## Summary

The Docker commands used in this activity demonstrated the basic container lifecycle, from downloading an image and creating a container to stopping and removing it. These operations are important for managing containerized applications in cloud-native environments.
