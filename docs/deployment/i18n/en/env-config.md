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
| `NEW_API_BASE_URL` | new-api upstream address | `http://localhost:3000` |
| `NEW_API_KEY` | new-api admin key | (Required) |
| `LOG_LEVEL` | Log level | `INFO` |

## Configuration File

Create a `.env` file:

```bash
APP_ENV=production
APP_PORT=8000
JWT_SECRET=your-secret-key
NEW_API_BASE_URL=http://localhost:3000
NEW_API_KEY=sk-your-new-api-key
```
