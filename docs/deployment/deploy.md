> 🌐 **语言 / Language**: [中文](deploy.md) | [English](i18n/en/deploy.md)

# 部署指南

## 生产环境要求

- Debian 13 (trixie) ARM64
- Nginx 或 Caddy（反向代理）
- 域名及 SSL 证书
- 2GB+ 内存
- Go >= 1.21（运行 new-api）

## 部署步骤

### 1. 更新系统

```bash
sudo apt update && sudo apt upgrade -y
```

### 2. 安装依赖

```bash
sudo apt install -y python3 python3-pip nginx golang-go
```

### 3. 部署 new-api 上游网关

```bash
# 克隆 new-api 仓库
git clone https://github.com/Calcium-Ion/new-api /opt/new-api
cd /opt/new-api

# 编译
go build -o new-api

# 配置 systemd 服务（参考 new-api 官方文档）
sudo systemctl enable new-api
sudo systemctl start new-api
```

> 详细配置请参考 [new-api 官方文档](https://gitcode.com/QuantumNous/new-api)。

### 4. 配置反向代理

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

### 5. 启动 Passnux 服务

```bash
# 使用 systemd 管理服务
sudo systemctl enable passnux
sudo systemctl start passnux
```