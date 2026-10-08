# Mission Reflection

## 1. How does writing a docker-compose.yml file make a cloud engineer's job easier compared to manually typing commands?

Writing a docker-compose.yml file means I describe my whole infrastructure once and then launch it with a single command. Without it, I would have to type a long `docker run` command for every container, with all the ports, environment variables, and network settings. That is slow and easy to get wrong. The file is also reusable and can be saved in GitHub, so another engineer can deploy the exact same setup.

## 2. What happens if you make an indentation error (like using a Tab instead of Spaces) in a YAML file?

YAML uses indentation to show how things are nested, and it does not accept tabs for that. If I use a Tab or the wrong number of spaces, Docker Compose cannot read the file and shows an error like "mapping values are not allowed here" instead of starting anything. A small spacing mistake can break the whole deployment, so I have to check my formatting carefully.

## 3. Why did we use environment variables (like MYSQL_PASSWORD) in the Compose file?

Environment variables let me configure a container without changing its image. MariaDB uses them to create the database, the user, and the passwords when it starts, and Nextcloud uses the same values to know how to log in to that database. This keeps the settings in one place and makes them easy to change for different deployments. In a real project, secrets like passwords should be stored more safely, but for this lab they showed how containers are configured.

## 4. How did it feel to deploy a fully functional enterprise cloud storage system (Nextcloud) in just a few minutes?

It felt amazing and a little surprising. I expected something this big to take hours of installing and configuring software. Instead, I wrote one file, ran `docker-compose up -d`, and had a working private cloud in a few minutes. It showed me how powerful containers are, and it made enterprise tools feel much more reachable.

## 5. How has your understanding of Cloud Computing evolved since Mission 1?

In Mission 1, I thought cloud computing mostly meant storing files online. Now I understand it is about building and managing infrastructure: running services, connecting them, and deploying them quickly and repeatably. I moved from simply using the cloud to actually building pieces of it, from single containers to a multi-tier system. I now see why automation and documentation matter so much to cloud engineers.
