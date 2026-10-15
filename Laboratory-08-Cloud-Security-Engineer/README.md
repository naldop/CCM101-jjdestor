# Laboratory 08 - Cloud Security Engineer

## Mission Overview

In this mission I acted as a Cloud Security Engineer. I deployed a simple Nginx web application in a container, confirmed it was reachable, and then secured the server with a host-based firewall (UFW). The firewall uses a default deny policy and only allows the traffic that is actually needed (SSH and the web app on port 8080).

## Objectives

- Set up the Laboratory-08 folder structure in my GitHub portfolio.
- Explain key security concepts: Principle of Least Privilege, Attack Surface, and Default Deny Policy.
- Deploy a web application (Nginx on port 8080) and verify it with curl.
- Configure UFW with a default deny policy while keeping SSH access.
- Open only the required port (8080/tcp) and verify the firewall works.
- Document the configuration and reflect on what I learned.

## Commands Executed

```bash
# Deploy the application
docker run -d --name secure-web-app -p 8080:80 nginx
curl localhost:8080

# Build the firewall
sudo ufw allow ssh
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw enable
sudo ufw status verbose

# Allow the web application port
sudo ufw allow 8080/tcp
sudo ufw status numbered
curl localhost:8080
```

## Skills Learned

- Running and testing a containerized web server with Docker and curl.
- Configuring a host-based firewall with UFW.
- Applying a default deny policy and creating specific allow rules.
- Reducing a server's attack surface by closing unused ports.
- Documenting technical work clearly in Markdown.
- Organizing and publishing lab work in a GitHub portfolio.
