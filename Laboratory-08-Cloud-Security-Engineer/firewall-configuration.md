# Firewall Configuration

Commands used to secure the `secure-web-app` server with UFW (Uncomplicated Firewall) on the KillerCoda Ubuntu Playground.

## 1. Allow SSH

```bash
sudo ufw allow ssh
```

Permanently allows SSH (port 22) so administrators can still manage the server remotely.

## 2. Set the Default Deny Policy

```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

Blocks all incoming traffic by default while still allowing the server to make outgoing connections.

## 3. Allow Port 8080

```bash
sudo ufw allow 8080/tcp
```

Creates a specific rule that lets TCP traffic reach the Nginx web application on port 8080.

## Why SSH Must Be Allowed Before Enabling UFW

If `sudo ufw enable` is run before allowing SSH, the default deny policy would immediately block port 22 and lock the administrator out of the server.
