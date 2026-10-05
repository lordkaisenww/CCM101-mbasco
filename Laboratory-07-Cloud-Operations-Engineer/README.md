# Laboratory 07 - Cloud Operations Engineer

## Mission Overview
In this laboratory, I act as a Cloud Operations Engineer who need to keep a small website healthy. First, I check the host server's memory, disk, and CPU so I know how the normal condition look like. After that, I install Nginx inside a Docker container, send some good and bad requests to it, then read the logs to see what happen. I learned that it is important to monitor a system first before something goes wrong.

## Objectives
- Check the baseline of the host server like RAM, disk storage, and CPU load.
- Run a web application using Docker and Nginx.
- Make sure the application is running and can be reach in port 8080.
- Try successful requests (HTTP 200) and a failed request (HTTP 404).
- Read the application logs to find the error.
- Save the screenshots and write the reports for the findings.

## Monitoring Commands Executed

| Command | Purpose | Evidence |
|---|---|---|
| `free -h` | Check the total and available memory (RAM) | `memory-check.png` |
| `df -h` | Check the disk size of the root (/) file system | `disk-check.png` |
| `top` | See the running processes and CPU load | - |
| `docker run -d --name client-website -p 8080:80 nginx` | Start the Nginx container and connect port 8080 to port 80 | `install-nginx.png` |
| `docker ps` | Check if the container is running | `install-nginx.png` |
| `ss -tlnp \| grep 8080` | Check if something is listening on port 8080 | - |
| `curl http://localhost:8080` (3 times) | Send successful requests (HTTP 200) | `simulation1.png` |
| `curl http://localhost:8080/hidden-admin-page` | Request a page that not exist (HTTP 404) | `simulation2.png` |
| `docker logs client-website` | See the request logs of the application | `docker-logs.png` |
| `docker logs client-website 2>&1 \| grep 404` | Filter the logs to show only the 404 line | - |

**Baseline values I got:** 1.9 GiB total RAM, 19 GB root file system (30% used), and the CPU is around 99% idle.

## Skills Learned
- How to read the output of `free -h`, `df -h`, and `top` to know if the server is healthy.
- How to run a web server inside Docker and open its port.
- How to test a website from the terminal using `curl`.
- The difference of HTTP status codes, where 200 is success and 404 is page not found.
- How to use `docker logs` with `grep` to find the exact line of an error.
- Why baseline and logs is important, because they show what is normal and what went wrong when a problem happen.
