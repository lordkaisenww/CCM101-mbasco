# Firewall Configuration

## 1. Allow SSH
```
sudo ufw allow ssh
```

This command allows SSH connections so we can access our server remotely. It helps us connect to the server using a secure connection. We need to allow SSH before enabling the firewall to avoid losing access. This is important because we can still manage and configure our server remotely.

## 2. Set the Default Deny Policy
```
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

These commands block all incoming connections by default and allow outgoing connections from our server. This means only the incoming connections that we allow can access our system. It helps protect our server from unauthorized users and possible attacks. By using this policy, we can make our server more secure.

## 3. Allow Port 8080
```
sudo ufw allow 8080/tcp
```

This command allows TCP traffic on port 8080 so we can access our web application. Port 8080 is commonly used for web applications and services. We need to allow this port so users can connect to our application. This helps our application work properly while the firewall is enabled.

## 4. What happens if `sudo ufw enable` runs before `sudo ufw allow ssh`?

If I run `sudo ufw enable` before allowing SSH, my SSH connection might get blocked by the firewall. This means I may lose remote access to my server. I might not be able to connect to my server again until the firewall settings are fixed. That is why it is important to allow SSH first before enabling the firewall.
