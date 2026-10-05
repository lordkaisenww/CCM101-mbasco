# Laboratory 06 - The Cloud Deployment Engineer

## Mission Overview
In this lab I played the role of a cloud deployment engineer. My job was to deploy a two-tier app using Docker Compose, with one container for the web app and one for the MySQL database. Instead of starting each container myself, I wrote a single `docker-compose.yml` file and let Compose do the work. After testing it, I shut everything down and saved my files with Git.

## Objectives
- Make a project folder and write a `docker-compose.yml` file.
- Set up the `app` and `db` services with their ports, environment variables, and volume.
- Start everything in the background with one command.
- Check that the containers were running and that the app could connect to the database.
- Stop and remove the containers when I was done.
- Save my project using Git.

## Commands Executed

| Command | What it does |
|---|---|
| `mkdir docker-lab06` | Makes a new folder for the project. |
| `cd docker-lab06` | Goes inside that folder. |
| `nano docker-compose.yml` | Opens the file in nano so I can write the Compose setup. |
| `docker-compose up -d` | Builds and starts all the services in the background. |
| `docker-compose ps` | Shows which containers are running. |
| `docker-compose down` | Stops and removes the containers and the network. |
| `git init` | Starts a Git repository in the folder. |
| `git add .` | Adds my files so they're ready to be saved. |
| `git commit -m "Add docker-compose setup"` | Saves my changes with a message. |
| `git push origin main` | Sends my commit to the remote repository. |

## Skills Learned
- How to write a `docker-compose.yml` file and what the `services:` block does.
- How containers find each other by service name, like `MYSQL_HOST: db`.
- How to run a whole multi-container app with one command instead of many `docker run` commands.
- How to check on containers with `docker-compose ps` and clean up with `docker-compose down`.
- How to use environment variables and volumes for settings and database data.
- How to use basic Git commands to save and share my work.
