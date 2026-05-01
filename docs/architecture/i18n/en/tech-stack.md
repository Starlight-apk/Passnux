> 🌐 **Language / 语言**: [English](tech-stack.md) | [中文](../../tech-stack.md)

# Tech Stack

> Passnux **does not implement its own AI model invocation**. All AI capabilities are provided by the upstream new-api gateway. Passnux focuses on the frontend UI, API proxy, user management, and quota distribution.

## Technology Decisions

### Frontend
| Option | Status | Description |
| :--- | :--- | :--- |
| Framework | TBD | Considering React / Vue3 |
| UI Library | TBD | Considering Tailwind CSS |
| Build Tool | TBD | Considering Vite |

### Backend
| Option | Status | Description |
| :--- | :--- | :--- |
| Language | TBD | Considering Python / Node.js |
| Framework | TBD | Considering FastAPI / Express |
| Runtime | TBD | Considering uvicorn / PM2 |

### Database
| Option | Status | Description |
| :--- | :--- | :--- |
| Primary DB | TBD | Considering PostgreSQL |
| Cache | TBD | Considering Redis |

### AI Gateway (Upstream)
| Option | Status | Description |
| :--- | :--- | :--- |
| Upstream Gateway | ✅ Confirmed | [new-api](https://github.com/Calcium-Ion/new-api) — Multi-model aggregation, load balancing, key management, quota control. Passnux forwards AI requests to this gateway via API proxy |

## ARM64 Compatibility

All technology choices must be verified for ARM64 compatibility and performance.
