> 🌐 **语言 / Language**: [中文](overview.md) | [English](i18n/en/overview.md)

# API 概览

## 基础信息

- **Base URL**: `https://api.passnux.org/v1`
- **数据格式**: JSON
- **字符编码**: UTF-8
- **上游网关**: 请求经 Passnux 后端转发至 [new-api](https://gitcode.com/QuantumNous/new-api) 统一调度

## 接口列表

| 方法 | 路径 | 说明 |
| :--- | :--- | :--- |
| POST | `/auth/login` | 用户登录 |
| POST | `/auth/register` | 用户注册 |
| GET  | `/models` | 获取模型列表（从 new-api 同步） |
| POST | `/chat/completions` | AI 对话（经 new-api 转发） |
| GET  | `/user/profile` | 获取用户信息 |

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