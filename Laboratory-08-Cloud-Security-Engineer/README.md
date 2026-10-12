# Laboratory 08 - Cloud Security Engineer

## Mission Overview

In this laboratory, our mission is to learn how to secure a cloud server using a host-based firewall called UFW (Uncomplicated Firewall). We configured firewall rules to control incoming and outgoing network traffic. We also learned how to allow SSH connections and port 8080 while blocking unauthorized connections. This activity helps us understand the importance of protecting our server from possible security threats.

## Objectives

1. Understand the importance of cloud security and firewall configuration.
2. Learn how to use UFW to manage network connections.
3. Apply the Default Deny Policy to block unauthorized incoming traffic.
4. Allow SSH connections for remote server access.
5. Configure port 8080 for web application access.
6. Learn how to reduce the attack surface of our server.

## Commands Executed

### 1. Allow SSH
```bash
sudo ufw allow ssh
```

### 2. Set the Default Deny Policy
```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

### 3. Allow Port 8080
```bash
sudo ufw allow 8080/tcp
```

### 4. Enable the Firewall
```bash
sudo ufw enable
```

### 5. Check Firewall Status
```bash
sudo ufw status
```

## Skills Learned

In this laboratory, I learned how to configure and manage a firewall using UFW commands in Linux. I also learned how to allow specific ports and block unnecessary incoming connections to protect our server. I understand why allowing SSH before enabling the firewall is important to avoid losing remote access. This activity helped me improve my basic knowledge of cloud security, network protection, and server management.
