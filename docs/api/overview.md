> 🌐 **语言 / Language**: [中文](overview.md) | [English](i18n/en/overview.md)

# API 概览

> Passnux 的 API 分为两类：**用户管理接口**（由 Passnux 自身处理）和 **AI 代理接口**（透传转发至上游 new-api）。

## 基础信息

- **Base URL**: `https://api.passnux.org/v1`
- **数据格式**: JSON
- **字符编码**: UTF-8
- **上游网关**: AI 相关请求经 Passnux 代理转发至 [new-api](https://gitcode.com/QuantumNous/new-api)

## 接口列表

### 用户管理（Passnux 自身处理）
| 方法 | 路径 | 说明 |
| :--- | :--- | :--- |
| POST | `/auth/login` | 用户登录 |
| POST | `/auth/register` | 用户注册 |
| POST | `/auth/refresh` | 刷新 Token |
| GET  | `/user/profile` | 获取用户信息 |
| GET  | `/user/quota` | 获取用户剩余额度 |

### AI 代理（转发至 new-api）
| 方法 | 路径 | 说明 |
| :--- | :--- | :--- |
| GET  | `/models` | 获取模型列表（从 new-api 同步） |
| POST | `/chat/completions` | AI 对话（透传转发至 new-api） |
| POST | `/v1/chat/completions` | OpenAI 兼容接口（透传转发至 new-api） |

## 通用响应格式

```json
{
  "code": 0,
  "message": "success",
  "data": {}
}
```

## 错误码

| 错误码 | 说明 |
| :--- | :--- |
| 0 | 成功 |
| 1001 | 参数错误 |
| 1002 | 认证失败 |
| 1003 | 频率限制 |
| 2001 | 模型不可用 |