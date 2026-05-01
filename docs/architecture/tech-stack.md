> 🌐 **语言 / Language**: [中文](tech-stack.md) | [English](i18n/en/tech-stack.md)

# 技术选型

> Passnux **不自研 AI 模型调用**，所有 AI 能力由上游 new-api 网关提供。Passnux 专注前端界面、API 代理、用户管理与额度分发。

## 技术栈决策

### 前端
| 方案 | 状态 | 说明 |
| :--- | :--- | :--- |
| 框架 | 待定 | 考虑 React / Vue3 |
| UI 库 | 待定 | 考虑 Tailwind CSS |
| 构建工具 | 待定 | 考虑 Vite |

### 后端
| 方案 | 状态 | 说明 |
| :--- | :--- | :--- |
| 语言 | 待定 | 考虑 Python / Node.js |
| 框架 | 待定 | 考虑 FastAPI / Express |
| 运行时 | 待定 | 考虑 uvicorn / PM2 |

### 数据库
| 方案 | 状态 | 说明 |
| :--- | :--- | :--- |
| 主库 | 待定 | 考虑 PostgreSQL |
| 缓存 | 待定 | 考虑 Redis |

### AI 网关（上游）
| 方案 | 状态 | 说明 |
| :--- | :--- | :--- |
| 上游网关 | ✅ 已确定 | [new-api](https://gitcode.com/QuantumNous/new-api) — 多模型聚合、负载均衡、密钥管理、额度控制。Passnux 通过 API 代理转发至此网关 |

## ARM64 兼容性

所有选型均需确认 ARM64 架构下的兼容性和性能表现。