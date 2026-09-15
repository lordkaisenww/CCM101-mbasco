# Mission Reflection

## 1. Boot time and setup: Docker vs. Virtual Machines

Docker is much faster to run because the container can start in just few seconds. In Virtual Machine, it can take minutes because you need to boot a complete operating system and configure the web server. Containers are faster because they don't need to boot another OS and initialize many drivers and system resources.

## 2. Why is port mapping (-p 8080:80) necessary?

The port mapping `-p 8080:80` is needed because the Nginx is running inside the container and it is using port 80. The container have its own network and the port 80 is not directly visible from the host. By using port mapping, I can access the Nginx from the host using port 8080.

## 3. What happens to data when you use docker rm?

When I use `docker rm`, the container is removed including its writable layer and the data inside it will not be saved. If I want the data to stay, I need to use Docker volumes or another persistent storage. This is different from a Virtual Machine because a VM normally have a persistent virtual disk where the data can remain.

## 4. How does containerization change DevOps?

Containerization makes DevOps easier because the application and its dependencies can be package together in one container. This can reduce the "works on my machine" problem because the same container can run in different environments. Instead of managing many servers directly, the operations team can focus more on managing containers and services.

## 5. How is your GitHub portfolio evolving?

My GitHub portfolio is becoming more organized because I already have Laboratory 1 to 4 with different cloud computing activities. Before, I only have basic understanding about cloud and now I learn more about cloud infrastructure, multi-cloud and Docker containers. This laboratory help me understand how applications can be deploy and manage using containers.

