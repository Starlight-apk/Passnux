> 🌐 **语言 / Language**: [中文](env-config.md) | [English](i18n/en/env-config.md)

# 环境变量配置

## 配置项列表

| 变量名 | 说明 | 默认值 |
| :--- | :--- | :--- |
| `APP_ENV` | 运行环境 | `development` |
| `APP_PORT` | 服务端口 | `8000` |
| `DATABASE_URL` | 数据库连接 | `sqlite:///data.db` |
| `REDIS_URL` | Redis 连接 | `redis://localhost:6379` |
| `JWT_SECRET` | JWT 密钥 | （必填） |
| `JWT_EXPIRES` | Token 过期时间 | `86400` |
| `AI_API_KEY` | AI 模型 API 密钥 | （必填） |
| `AI_BASE_URL` | AI 模型 API 地址 | `https://api.deepseek.com` |
| `LOG_LEVEL` | 日志级别 | `INFO` |

## 配置文件

创建 `.env` 文件：

```bash
APP_ENV=production
APP_PORT=8000
JWT_SECRET=your-secret-key
AI_API_KEY=sk-your-api-key