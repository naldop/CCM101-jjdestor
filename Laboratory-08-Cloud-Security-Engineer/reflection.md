# Reflection

## 1. How does a host-based firewall protect a server if the physical network perimeter is breached?

A host-based firewall runs on the server itself, so it keeps filtering traffic even when the network around it is compromised. An attacker who gets past the perimeter still has to get through the server's own rules before reaching any service. It is a second layer of defense, so one failure does not expose everything.

## 2. Why is managing open network ports critical to reducing a server's attack surface?

Every open port is a door into a running service, and every service can have bugs or weak settings. By closing everything except what is needed, such as SSH and port 8080, there are fewer doors for an attacker to try. Fewer exposed services also means less to patch and monitor.

## 3. Why is it dangerous to leave a database port (like 3306 for MySQL) open to the public internet?

Anyone in the world could try to connect and attempt password guessing or known exploits. Databases hold sensitive data such as customer records and credentials, so one breach could mean data theft, ransomware, or legal trouble. A database should only be reachable from the application servers that need it, over a private network.

## 4. How did this mission change your perspective on how easily a server can be compromised?

Before this lab, I assumed a running web server was reasonably safe. I saw that the Nginx app was reachable with a single command, and that without a firewall every other port was open too. It showed me that servers are exposed by default, and security has to be added on purpose.

## 5. How does your GitHub portfolio currently look with eight completed missions?

My portfolio now has eight organized lab folders, each with a README, documentation, and screenshots. It shows steady progress from basic cloud tasks to security work, and it is proof of hands-on practice, not just theory.
