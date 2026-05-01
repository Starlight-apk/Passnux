> 🌐 **Language / 语言**: [English](overview.md) | [中文](../../overview.md)

# API Overview

> Passnux APIs are divided into two categories: **User Management APIs** (handled by Passnux itself) and **AI Proxy APIs** (transparently forwarded to upstream new-api).

## Basic Information

- **Base URL**: `https://api.passnux.org/v1`
- **Data Format**: JSON
- **Character Encoding**: UTF-8
- **Upstream Gateway**: AI-related requests are proxied through Passnux to [new-api](https://github.com/Calcium-Ion/new-api)

## Endpoints

### User Management (Handled by Passnux)
| Method | Path | Description |
| :--- | :--- | :--- |
| POST | `/auth/login` | User login |
| POST | `/auth/register` | User registration |
| POST | `/auth/refresh` | Refresh token |
| GET  | `/user/profile` | Get user profile |
| GET  | `/user/quota` | Get user remaining quota |

### AI Proxy (Forwarded to new-api)
| Method | Path | Description |
| :--- | :--- | :--- |
| GET  | `/models` | List available models (synced from new-api) |
| POST | `/chat/completions` | AI chat completion (proxied to new-api) |
| POST | `/v1/chat/completions` | OpenAI-compatible endpoint (proxied to new-api) |

## Common Response Format

```json
{
  "code": 0,
  "message": "success",
  "data": {}
}
```

## Error Codes

| Code | Description |
| :--- | :--- |
| 0 | Success |
| 1001 | Invalid parameters |
| 1002 | Authentication failed |
| 1003 | Rate limit exceeded |
| 2001 | Model unavailable |
