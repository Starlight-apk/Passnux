> 🌐 **Language / 语言**: [English](deploy.md) | [中文](../../deploy.md)

# Deployment Guide

## Production Requirements

- Debian 13 (trixie) ARM64
- Nginx or Caddy (reverse proxy)
- Domain name and SSL certificate
- 2GB+ RAM

## Deployment Steps

### 1. Update System

```bash
sudo apt update && sudo apt upgrade -y
```

### 2. Install Dependencies

```bash
sudo apt install -y python3 python3-pip nginx
```

### 3. Configure Reverse Proxy

```nginx
server {
    listen 443 ssl;
    server_name api.passnux.org;

    location / {
        proxy_pass http://127.0.0.1:8000;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
    }
}
```

### 4. Start Service

```bash
# Use systemd to manage the service
sudo systemctl enable passnux
sudo systemctl start passnux
```
