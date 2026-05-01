> 🌐 **Language / 语言**: [English](overview.md) | [中文](../../overview.md)

# Architecture Overview

## Overall Architecture

Passnux adopts a front-end/back-end separation architecture. AI capabilities are provided by the upstream [new-api](https://github.com/Calcium-Ion/new-api) gateway. Passnux itself **does not directly call any AI models** — it only provides the frontend UI, API proxy forwarding, user management, and quota distribution:

```
┌─────────────┐     ┌──────────────┐     ┌──────────────────┐     ┌─────────────┐
│  Frontend   │────▶│  Passnux     │────▶│  new-api (Upstr) │────▶│  AI Models  │
│  (Web UI)   │◀────│  API Proxy   │◀────│  AI Gateway      │     │ (Vendors)   │
└─────────────┘     └──────────────┘     └──────────────────┘     └─────────────┘
                     │    │    │
              ┌──────┘    │    └──────┐
              ▼           ▼           ▼
         ┌────────┐ ┌──────────┐ ┌────────┐
         │  User  │ │  Quota   │ │ Chat   │
         │  Mgmt  │ │  Distr.  │ │ History│
         └────────┘ └──────────┘ └────────┘
```

## Core Components

| Component | Responsibility | Technology |
| :--- | :--- | :--- |
| Frontend | User interface (AI chat, model switching) | TBD |
| Backend | API proxy, user management, quota distribution | TBD |
| Database | User data, chat history, quota records | TBD |
| AI Gateway (Upstream) | Model aggregation, load balancing, key management | [new-api](https://github.com/Calcium-Ion/new-api) |

## Design Principles

1. **Modularity** — Low coupling, high cohesion
2. **Scalability** — Horizontal scaling support
3. **Security** — Encrypted data transmission
4. **ARM64 Optimization** — Leverage ARM architecture features
