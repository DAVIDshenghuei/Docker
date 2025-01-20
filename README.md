# Docker Commands Reference Guide

This document provides a comprehensive guide to commonly used Docker commands, along with their functionalities and usage examples. Whether you are starting with Docker or need a quick refresher, this guide has you covered.

Table of Contents

Downloading and Running Docker Images

Managing Containers

Copying Files

Exporting and Importing Images

Advanced Commands

Downloading and Running Docker Images

Pull an Image

docker pull [image]:[version]

Downloads a specific image and version to your local system.

Run an Image

docker run [image]:[version]

Runs the specified image. If the image is not available locally, it will download it first.

Managing Containers

Check Running Containers

List currently running containers:

docker ps

List the last [number] of containers:

docker ps -n [number]

List all containers:

docker ps -a

List container IDs only:

docker ps -q

Rename a Container

docker run --name=[new_name] [image] /bin/bash

Assigns a custom name to a container.

Start an Image with Command Prompt

docker run -it [image] /bin/bash

Exit the container: Use exit to close the container.

Detach from the container without closing: Use Ctrl + P + Q.

Restart a Stopped Container

docker start [CONTAINER ID]

Stop a Container

docker stop [CONTAINER ID]

Delete Containers and Images

Delete a stopped container:

docker rm [CONTAINER ID]

Delete an image:

docker rmi [image]

Force delete a container:

docker rm -f [CONTAINER ID]

Copying Files

Copy Files Between Host and Container

docker cp [CONTAINER ID]:[container_path] [host_path]

Example:

docker cp [CONTAINER ID]:/path/to/file /host/destination

Exporting and Importing Images

Export a Container as a TAR File

docker export [CONTAINER ID] > [file_name.tar]

Import an Image from a TAR File

cat [file_name.tar] | docker import - [image_user]/[image_name]:[version]

Advanced Commands

Inspect Container Details

docker inspect [CONTAINER ID]

View Container Logs

docker logs [CONTAINER ID]

Monitor Running Processes

docker top [CONTAINER ID]

Pause and Unpause Containers

Pause:

docker pause [CONTAINER ID]

Unpause:

docker unpause [CONTAINER ID]

Tagging and Pushing Images

Add a tag to an image:

docker tag [image] [repository]:[tag]

Push an image to Docker Hub:

docker push [repository]:[tag]

Additional Information

This guide includes both basic and advanced Docker commands to help streamline your container management workflow. For more detailed explanations, refer to the official Docker documentation.

Happy Dockering!

