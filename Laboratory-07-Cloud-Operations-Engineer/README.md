# Laboratory 07: Cloud Operations Engineer

## Mission Overview

In this lab, I acted as a Cloud Operations Engineer. I established a health baseline for a host server, deployed a client's Nginx web server in a Docker container, generated traffic to test it, and monitored it through application logs and real-time resource metrics.

## Objectives

- Create an organized lab folder in my GitHub repository.
- Establish a baseline of the host server's memory, disk, and CPU health.
- Deploy an Nginx web server container and simulate user traffic.
- Use application logs to identify successful requests and errors.
- Monitor the container's CPU and memory usage in real time.
- Document findings and reflect on the difference between logging and monitoring.

## Monitoring Commands Executed

| Command | Purpose |
|---------|---------|
| `free -h` | Check the server's memory (RAM) usage |
| `df -h` | Check available disk storage |
| `top` | View running processes and CPU load |
| `docker run -d -p 8080:80 --name client-website nginx` | Deploy the Nginx web server in the background on port 8080 |
| `curl http://localhost:8080` | Simulate a user visiting the website |
| `curl http://localhost:8080/hidden-admin-page` | Generate a 404 error by requesting a page that doesn't exist |
| `docker logs client-website` | Retrieve the container's application logs |
| `docker stats` | View live CPU, memory, and network usage of the container |

## Skills Learned

- Establishing a host system baseline before deploying applications.
- Deploying and naming containers with Docker.
- Simulating traffic with `curl`.
- Reading application logs to tell successful requests (200) from errors (404).
- Monitoring container resource usage with `docker stats`.
- Documenting technical work in Markdown and organizing it in GitHub.
