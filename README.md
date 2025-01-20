# Docker Command Notebook

This document serves as a comprehensive guide to commonly used Docker commands, helping you manage images, containers, and more efficiently.

## Purpose

This notebook is designed to:

1. Help users understand key Docker commands.

2. Serve as a quick reference for daily Docker operations.

3. Provide examples and explanations for container management.

## Quick Guide to Docker Commands

### Managing Images

Download an image:

    docker pull [image]:[version]

Delete an image: 

    docker rmi [image]

Export an image:

    docker export [CONTAINER ID] > [filename.tar]

Import an image: 

    cat [filename.tar] | docker import - [user]/[image]:[version]

### Running Containers

Start a container:

    docker run [image]:[version]

Start with a command-line interface:

    docker run -it [image] /bin/bash

Start a stopped container:

    docker start [CONTAINER ID]

Restart a container:

    docker restart [CONTAINER ID]

Stop a container:

    docker stop [CONTAINER ID]

Force stop and remove:

    docker rm -f [CONTAINER ID]

Rename a container:

    docker run --name=[new_name] [image]

### Container Status and Logs

Check running containers: 

    docker ps

Check all containers:

    docker ps -a

Fetch logs:

    docker logs [CONTAINER ID]

Inspect detailed information: 

    docker inspect [CONTAINER ID]

### Working with Container Files

Copy files from container to host:

    docker cp [CONTAINER ID]:[container_path] [host_path]

View filesystem changes:

    docker diff [CONTAINER ID]

### Container Operations

Attach to a running container:

    docker attach [CONTAINER ID]

Run a command in a container:

    docker exec -it [CONTAINER ID] /bin/bash

Pause a container: 

    docker pause [CONTAINER ID]

Unpause a container:

    docker unpause [CONTAINER ID]

### Saving and Loading Images

Save an image: 

    docker save [image] > [filename.tar]

Load an image:

    docker load < [filename.tar]

### Searching and Tagging Images

Search for an image: 

    docker search [term]

Tag an image:

    docker tag [image] [repository]:[tag]

### Additional Notes

Use docker info to view system-wide information about your Docker setup.

Use docker version to check the version of your Docker installation.

To troubleshoot issues, inspect containers with docker inspect or view logs using docker logs.

Tips for Managing Containers

To detach from a running container without stopping it, use 

    Ctrl + P + Q.

If a container is using an image you want to delete, you must remove the container first.

Happy Dockering!

