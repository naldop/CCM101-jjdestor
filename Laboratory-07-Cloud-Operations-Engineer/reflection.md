# Mission Reflection

## 1. Why check the host server's resources even if containers are running perfectly?

Containers share the host's CPU, memory, and disk, so they are only as healthy as the server underneath them. A container can look fine while the host is quietly running out of resources. For example, a full disk can stop logs from being written and crash applications, and low memory can cause containers to be killed without warning. Checking the host gives me a baseline to compare against, so I can spot problems early and prepare for traffic surges before users are affected.

## 2. How would docker logs help if a user cannot log in?

Running `docker logs` on the container would show me exactly what happened when the user tried to log in. I could find the user's request, see whether it reached the application, and check the status code it returned. A 401 or 403 would suggest a credentials or permissions problem, a 404 would suggest a wrong page or broken route, and a 500 would point to an error inside the application. Timestamps would let me match the complaint to specific log entries, so I could find the cause instead of guessing.

## 3. What is the difference between logging (Checkpoint 4) and monitoring (Checkpoint 5)?

Logging records individual events, such as each request and its result. It works like security camera footage: it tells me what happened and why after something goes wrong. Monitoring tracks the container's resource usage, such as CPU, memory, and network traffic, in real time with `docker stats`. It works like a dashboard that shows how healthy the system is right now. Logs are best for troubleshooting specific errors, while monitoring is best for spotting overload or unusual usage before it causes failures. A good cloud operations engineer uses both together.
