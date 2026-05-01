> 🌐 **Language / 语言**: [English](deploy.md) | [中文](../../deploy.md)

# Deployment Guide

## Production Requirements

- Debian 13 (trixie) ARM64
- Nginx or Caddy (reverse proxy)
- Domain name and SSL certificate
- 2GB+ RAM
- Go >= 1.21 (for running new-api)

## Deployment Steps

### 1. Update System

```bash
sudo apt update && sudo apt upgrade -y
```

### 2. Install Dependencies

```bash
sudo apt install -y python3 python3-pip nginx golang-go
```

### 3. Deploy new-api Upstream Gateway

```bash
# Clone new-api repository
git clone https://github.com/Calcium-Ion/new-api /opt/new-api
cd /opt/new-api

# Build
go build -o new-api

# Configure systemd service (refer to new-api docs)
sudo systemctl enable new-api
sudo systemctl start new-api
```

> For detailed configuration, refer to the [new-api documentation](https://github.com/Calcium-Ion/new-api).

### 4. Configure Reverse Proxy

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

### 5. Start Passnux Service

```bash
# Use systemd to manage the service
sudo systemctl enable passnux
sudo systemctl start passnux
```
