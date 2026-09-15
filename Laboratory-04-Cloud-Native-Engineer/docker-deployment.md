# Docker Deployment Log

## Commands Used and What They Did

1. `docker ps` – Lists all currently running containers.
2. `docker stop my-nginx` – Gracefully stops the running Nginx container by sending it a shutdown signal.
3. `docker ps -a` – Lists all containers, including stopped ones, to confirm `my-nginx` shows an "Exited" status.
4. `docker rm my-nginx` – Permanently removes the stopped container and its filesystem layer from the system.

![Container Lifecycle](./screenshots/container-lifecycle.png)
