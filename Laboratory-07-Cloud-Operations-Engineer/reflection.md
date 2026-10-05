# Mission Reflection

**1. Why check the host server's resources?**
Even if my containers are running perfectly, I still need to check the host server because the containers use the resources of the host. If the RAM or disk of the host is almost full, the containers can become slow or crash suddenly. In this lab, my host has 1.9 GiB of RAM and 19 GB of disk, so I know how much space I have before a problem happen.

**2. How does docker logs help when a user cannot log in?**
I will run docker logs to see the requests and errors of the application. The logs show the status codes and the time, like the 404 I saw in this lab. With this, I can find if the problem is a wrong URL, a server error, or something else, instead of just guessing.

**3. Logs vs. metrics**
Logs are the record of events that already happened, like each request and error. Metrics are numbers that are measured over time, like CPU and memory usage. Logs tell me what happened, while metrics tell me how healthy the system is.

**4. How do big companies monitor thousands of containers?**
I think big companies cannot check thousands of containers by hand. They use tools like Prometheus to collect the metrics automatically, and Grafana to show them in dashboards with graphs. They can also set alerts, so the team know right away when something go wrong.

**5. How did my troubleshooting improve?**
My troubleshooting in Linux is improved a lot. Before, I only know the basic commands, but now I can read free -h, df -h, and top to understand the health of the server. I also learned how to use docker logs and grep to find a specific error. One mistake I made was pasting all the commands at once, so the curl showed "Connection reset by peer" because Nginx was not ready yet. From that, I learned to run the commands one by one and check the result first.
