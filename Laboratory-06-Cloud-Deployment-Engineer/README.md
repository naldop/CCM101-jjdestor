# Laboratory 06: Cloud Deployment Engineer

## Mission Overview

In this mission, I acted as a Cloud Deployment Engineer and deployed a private cloud storage system using a multi-container architecture. I wrote a `docker-compose.yml` file that defines two services: a MariaDB database container and a Nextcloud application container. With one command, Docker Compose pulled the images, connected the containers on a shared network, and started the whole stack. I then accessed the Nextcloud setup page in the browser and shut everything down cleanly.

## Objectives

- Explain what a two-tier architecture is and why the web tier and database tier are separated
- Write a `docker-compose.yml` file to define a multi-container application
- Deploy and manage multiple containers using Docker Compose
- Connect an application container to a database container using service names and environment variables
- Access a running containerized application through a browser
- Document the deployment process and reflect on what I learned

## Commands Executed

```bash
mkdir nextcloud-deployment
cd nextcloud-deployment
nano docker-compose.yml
docker-compose up -d
docker-compose ps
docker-compose down
```

## Skills Learned

- Writing and debugging YAML configuration files (indentation-sensitive, spaces only)
- Defining multi-service applications with Docker Compose
- Using environment variables to configure containers
- Using service names as hostnames for container-to-container networking
- Deploying a two-tier application (web/application tier and database tier)
- Exposing container ports to access an application in the browser
- Cleanly shutting down and removing infrastructure with `docker-compose down`
- Documenting technical work in Markdown and managing it with Git and GitHub
