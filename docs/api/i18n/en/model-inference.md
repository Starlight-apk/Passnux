> 🌐 **Language / 语言**: [English](model-inference.md) | [中文](../../model-inference.md)

# Model Inference API

> Passnux **does not implement its own AI model invocation**. This endpoint is a transparent proxy — all requests are forwarded to the upstream [new-api](https://github.com/Calcium-Ion/new-api) gateway.

## AI Chat (Proxy)

```
POST /v1/chat/completions
```

**Request Headers:**
```
Authorization: Bearer <token>
Content-Type: application/json
```

**Request Body:**
```json
{
  "model": "deepseek-chat",
  "messages": [
    {"role": "user", "content": "Hello"}
  ],
  "stream": false
}
```

**Response:**

Response format is OpenAI API compatible, returned by new-api.

## Supported Models

Models are managed by the upstream [new-api](https://github.com/Calcium-Ion/new-api) gateway, supporting but not limited to:

| Model | Description |
| :--- | :--- |
| `deepseek-chat` | DeepSeek chat model |
| `gpt-3.5-turbo` | OpenAI GPT-3.5 |
| `gpt-4o` | OpenAI GPT-4o |
| `qwen-turbo` | Tongyi Qianwen |
| `claude-3-haiku` | Anthropic Claude 3 |

> 💡 The actual available model list depends on new-api admin configuration. Use `GET /models` to get the real-time list.

## Streaming Output

Set `stream: true` to enable SSE streaming output (natively supported by new-api).
