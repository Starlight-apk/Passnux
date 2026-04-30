# 认证鉴权

## 认证方式

采用 JWT (JSON Web Token) 进行用户认证。

## 获取 Token

```
POST /v1/auth/login
```

**请求体：**
```json
{
  "username": "user@example.com",
  "password": "your_password"
}
```

**响应：**
```json
{
  "code": 0,
  "data": {
    "token": "eyJhbGciOiJIUzI1NiIs...",
    "expires_in": 86400
  }
}
```

## 使用 Token

在请求头中携带：

```
Authorization: Bearer <your_token>
```

## Token 刷新

```
POST /v1/auth/refresh
```

有效期过期后需重新登录获取新 Token。