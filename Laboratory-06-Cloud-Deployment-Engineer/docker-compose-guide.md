# Docker Compose Guide

## The docker-compose.yml File

```yaml
version: '3'

services:
  database:
    image: mariadb:10.6
    environment:
      - MYSQL_ROOT_PASSWORD=cloudnova_root
      - MYSQL_PASSWORD=cloudnova_pass
      - MYSQL_DATABASE=nextcloud_db
      - MYSQL_USER=nextcloud_user

  app:
    image: nextcloud
    ports:
      - 8080:80
    environment:
      - MYSQL_PASSWORD=cloudnova_pass
      - MYSQL_DATABASE=nextcloud_db
      - MYSQL_USER=nextcloud_user
      - MYSQL_HOST=database
```

## What does the `services:` block do?

The `services:` block is where I list all the containers my application needs. Each thing under it, like `database` and `app`, is one service with its own image, ports, and settings. When I run Compose, it reads this block and starts one container for each service, so I don't have to start them one by one.

## How did the app container find the database?

The app found the database by using the name `database`. Compose puts all the services on the same network, and every service name works like a hostname there. In the app service I set `MYSQL_HOST=database`, so when Nextcloud tries to connect to `database`, Docker figures out the right container for it. I never had to type an IP address, which is good because the IP can change.

## docker run vs docker-compose up -d

`docker run` only starts one container, and I have to type all the options myself (ports, environment variables, network, and so on). With two or more containers that gets long and messy. `docker-compose up -d` starts everything in the file with a single command, and the `-d` makes it run in the background so I can still use my terminal. It's also easier to repeat because everything is saved in the file.
