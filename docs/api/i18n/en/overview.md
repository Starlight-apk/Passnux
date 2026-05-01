> 🌐 **Language / 语言**: [English](overview.md) | [中文](../../overview.md)

# API Overview

## Basic Information

- **Base URL**: `https://api.passnux.org/v1`
- **Data Format**: JSON
- **Character Encoding**: UTF-8

## Endpoints

| Method | Path | Description |
| :--- | :--- | :--- |
| POST | `/auth/login` | User login |
| POST | `/auth/register` | User registration |
| GET  | `/models` | List available models |
| POST | `/chat/completions` | AI chat completion |
| GET  | `/user/profile` | Get user profile |

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
