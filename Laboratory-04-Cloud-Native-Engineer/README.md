
# Laboratory 4: Cloud-Native Engineer

## Mission Overview

As part of the Cloud-Native Engineering Team at CloudNova Technologies, this laboratory explore the difference between traditional Virtual Machine and containerization. Using Docker in KillerCoda Playground, I deployed a live Nginx web server using container. This activity show how container can start faster and use less resources compare to traditional VM.

## Objectives

- To differentiate traditional Virtual Machines (VMs) and Containers.
- To access a Docker environment using KillerCoda.
- To execute basic Docker commands.
- To pull, run, manage, and stop a Nginx container.
- To create a technical documentation using Markdown.
- To continue building my GitHub Cloud Computing Portfolio.

## Docker Commands Executed

**Checkpoint 3 — Checking Docker**

- `docker --version` — Check if Docker is installed and show the Docker version.
- `docker info` — Shows information about the Docker environment, containers, images, and Docker daemon.

**Checkpoint 4 — Deploying Nginx**

- `docker pull nginx` — Downloads the Nginx image from Docker Hub.
- `docker run -d -p 8080:80 --name my-nginx nginx` — Runs the Nginx container in detached mode. It also connect the host port 8080 to container port 80.
- `curl http://localhost:8080` — Used to check if the Nginx web server is working correctly.

## Checkpoint 5 — Container Lifecycle

- `docker ps` — Shows the containers that is currently running.
- `docker stop my-nginx` — Stops the running Nginx container.
- `docker ps -a` — Shows all containers including the stopped container.
- `docker rm my-nginx` — Removes the Nginx container.

## Skills Learned

- I learned the difference between Virtual Machines and Containers.
- I learned how to use basic Docker CLI commands.
- I learned how port mapping works between host and container.
- I learned how to run, stop, check, and remove a container.
- I also learned how to make a simple technical documentation using Markdown.

## Challenges Encountered

One challenge I encountered is remembering the correct Docker command and the use of the `-p` port mapping. At first, I was confused about which port is for the host and which port is for the container. I also need to understand the detached mode because the container is running in the background even if the command is already finish.

Overall, this laboratory help me understand how Docker containers works and how it can be use for deploying applications faster and easier.

