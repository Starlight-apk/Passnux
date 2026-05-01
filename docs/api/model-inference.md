> 🌐 **语言 / Language**: [中文](model-inference.md) | [English](i18n/en/model-inference.md)

# 模型调用接口

> Passnux **不自研 AI 模型调用**。此接口为透传代理，所有请求转发至上游 [new-api](https://gitcode.com/QuantumNous/new-api) 网关处理。

## AI 对话（代理转发）

```
POST /v1/chat/completions
```

**请求头：**
```
Authorization: Bearer <token>
Content-Type: application/json
```

**请求体：**
```json
{
  "model": "deepseek-chat",
  "messages": [
    {"role": "user", "content": "你好"}
  ],
  "stream": false
}
```

**响应：**

响应格式与 OpenAI API 兼容，由 new-api 返回。

## 支持模型

模型由上游 [new-api](https://gitcode.com/QuantumNous/new-api) 网关统一管理，支持包括但不限于以下模型：

| 模型 | 说明 |
| :--- | :--- |
| `deepseek-chat` | DeepSeek 对话模型 |
| `gpt-3.5-turbo` | OpenAI GPT-3.5 |
| `gpt-4o` | OpenAI GPT-4o |
| `qwen-turbo` | 通义千问 |
| `claude-3-haiku` | Anthropic Claude 3 |

> 💡 实际可用模型列表以 new-api 管理后台配置为准，可通过 `GET /models` 接口获取实时列表。

## 流式输出

设置 `stream: true` 即可启用 SSE 流式输出（由 new-api 原生支持）。