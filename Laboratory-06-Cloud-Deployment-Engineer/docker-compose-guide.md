# Docker Compose Guide

## The docker-compose.yml File

```yaml
services:
  db:
    image: mysql:8.0
    container_name: mysql-db
    environment:
      MYSQL_ROOT_PASSWORD: rootpass
      MYSQL_DATABASE: appdb
      MYSQL_USER: appuser
      MYSQL_PASSWORD: apppass
    volumes:
      - db_data:/var/lib/mysql

  app:
    build: .
    container_name: web-app
    ports:
      - "5000:5000"
    environment:
      MYSQL_HOST: db
      MYSQL_DATABASE: appdb
      MYSQL_USER: appuser
      MYSQL_PASSWORD: apppass
    depends_on:
      - db

volumes:
  db_data:
```

## What does the `services:` block do?
The `services:` block is where I list all the containers my app needs. Each thing under it, like `db` and `app`, is one service with its own image, ports, and settings. When I run Compose, it reads this block and starts one container for each service, so I don't have to start them one by one.

## How did the app container find the database?
The app found the database by using the name `db`. Compose puts all the services on the same network, and every service name works like a hostname there. In the app service I set `MYSQL_HOST: db`, so when the app tries to connect to `db`, Docker figures out the right container for it. I never had to type an IP address, which is good because the IP can change.

## docker run vs docker-compose up -d
`docker run` only starts one container, and I have to type all the options myself (ports, environment variables, network, and so on). With two or more containers that gets long and messy. `docker-compose up -d` starts everything in the file with a single command, and the `-d` makes it run in the background so I can still use my terminal. It's also easier to repeat because everything is saved in the file.
