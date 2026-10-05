# Mission Reflection

Writing a docker-compose.yml file makes a cloud engineer's job a lot easier than typing commands by hand. With plain `docker run`, I would need a long command for every container, and I would have to remember all the ports, passwords, and network settings each time. With Compose, everything is written once in a file, and one command like `docker-compose up -d` starts the whole system.

YAML is very strict about spacing. If I use a Tab instead of spaces, Compose gives an error and refuses to start, because YAML only accepts spaces for indentation. Even using the wrong number of spaces can move a setting under the wrong section, so the file either fails or does not work the way I wanted. Now I always check my indentation first.

We used environment variables like MYSQL_PASSWORD so the database and the app could be configured without changing the image itself. They let me set the username, password, and database name in one place, and the app container uses the same values to connect. This is also better for security and flexibility, because I can change the values for a different environment without rewriting the code.

Deploying a working Nextcloud cloud storage system in just a few minutes felt amazing, and honestly a little unreal. I expected something like this to take hours of installing and configuring a server. Seeing the login page load after one command made me feel like a real cloud engineer.

My understanding of cloud computing has changed a lot since Mission 1. At first I thought the cloud was just "someone else's computer" for storing files. Now I see it is about building, connecting, and automating services that can be created, copied, and removed quickly. Tools like Docker and Compose show how much of the work can be written as code, and that idea of automation is what I will remember most.
