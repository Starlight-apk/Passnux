> 🌐 **语言 / Language**: [中文](env-config.md) | [English](i18n/en/env-config.md)

# 环境变量配置

> Passnux 自身不持有任何 AI 模型密钥，所有 AI 请求通过 `NEW_API_BASE_URL` 转发至上游 new-api 网关。

## 配置项列表

| 变量名 | 说明 | 默认值 |
| :--- | :--- | :--- |
| `APP_ENV` | 运行环境 | `development` |
| `APP_PORT` | 服务端口 | `8000` |
| `DATABASE_URL` | 数据库连接 | `sqlite:///data.db` |
| `REDIS_URL` | Redis 连接 | `redis://localhost:6379` |
| `JWT_SECRET` | JWT 密钥 | （必填） |
| `JWT_EXPIRES` | Token 过期时间 | `86400` |
| `NEW_API_BASE_URL` | new-api 上游地址（Passnux 将 AI 请求转发至此） | `http://localhost:3000` |
| `NEW_API_KEY` | new-api 管理密钥（用于同步模型列表等管理操作） | （必填） |
| `LOG_LEVEL` | 日志级别 | `INFO` |

## 配置文件

创建 `.env` 文件：

```bash
APP_ENV=production
APP_PORT=8000
JWT_SECRET=your-secret-key
NEW_API_BASE_URL=http://localhost:3000
NEW_API_KEY=sk-your-new-api-key
```