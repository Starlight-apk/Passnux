> 🌐 **Language / 语言**: [English](authentication.md) | [中文](../../authentication.md)

# Authentication

## Auth Method

JWT (JSON Web Token) is used for user authentication.

## Get Token

```
POST /v1/auth/login
```

**Request Body:**
```json
{
  "username": "user@example.com",
  "password": "your_password"
}
```

**Response:**
```json
{
  "code": 0,
  "data": {
    "token": "eyJhbGciOiJIUzI1NiIs...",
    "expires_in": 86400
  }
}
```

## Using the Token

Include it in the request header:

```
Authorization: Bearer <your_token>
```

## Token Refresh

```
POST /v1/auth/refresh
```

After expiration, you need to log in again to get a new token.
