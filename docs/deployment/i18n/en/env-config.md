> 🌐 **Language / 语言**: [English](env-config.md) | [中文](../../env-config.md)

# Environment Configuration

## Configuration Items

| Variable | Description | Default |
| :--- | :--- | :--- |
| `APP_ENV` | Runtime environment | `development` |
| `APP_PORT` | Service port | `8000` |
| `DATABASE_URL` | Database connection | `sqlite:///data.db` |
| `REDIS_URL` | Redis connection | `redis://localhost:6379` |
| `JWT_SECRET` | JWT secret key | (Required) |
| `JWT_EXPIRES` | Token expiration time | `86400` |
| `AI_API_KEY` | AI model API key | (Required) |
| `AI_BASE_URL` | AI model API base URL | `https://api.deepseek.com` |
| `LOG_LEVEL` | Log level | `INFO` |

## Configuration File

Create a `.env` file:

```bash
APP_ENV=production
APP_PORT=8000
JWT_SECRET=your-secret-key
AI_API_KEY=sk-your-api-key
```
