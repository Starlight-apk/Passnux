> 🌐 **Language / 语言**: [English](model-inference.md) | [中文](../../model-inference.md)

# Model Inference API

## AI Chat

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
```json
{
  "code": 0,
  "data": {
    "id": "chat-xxxx",
    "model": "deepseek-chat",
    "choices": [
      {
        "index": 0,
        "message": {
          "role": "assistant",
          "content": "Hello! How can I help you?"
        }
      }
    ]
  }
}
```

## Supported Models

| Model | Description |
| :--- | :--- |
| `deepseek-chat` | DeepSeek chat model |
| `gpt-3.5-turbo` | OpenAI GPT-3.5 |
| `qwen-turbo` | Tongyi Qianwen |

## Streaming Output

Set `stream: true` to enable SSE streaming output.
