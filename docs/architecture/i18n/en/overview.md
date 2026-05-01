> 🌐 **Language / 语言**: [English](overview.md) | [中文](../../overview.md)

# Architecture Overview

## Overall Architecture

Passnux adopts a front-end/back-end separation architecture, using [new-api](https://github.com/Calcium-Ion/new-api) as the upstream AI gateway for unified model request routing:

```
┌─────────────┐     ┌──────────────┐     ┌──────────────────┐     ┌─────────────┐
│  Frontend   │────▶│  Backend API │────▶│  new-api         │────▶│  AI Models  │
│  (Web UI)   │◀────│  (Service)   │◀────│  (AI Gateway)    │     │ (Vendors)   │
└─────────────┘     └──────────────┘     └──────────────────┘     └─────────────┘
                           │
                    ┌──────┴──────┐
                    │  Database   │
                    └─────────────┘
```

## Core Components

| Component | Responsibility | Technology |
| :--- | :--- | :--- |
| Frontend | User interface | TBD |
| Backend | Business logic | TBD |
| Database | Data persistence | TBD |
| AI Gateway | Model aggregation, load balancing, key management | [new-api](https://github.com/Calcium-Ion/new-api) |

## Design Principles

1. **Modularity** — Low coupling, high cohesion
2. **Scalability** — Horizontal scaling support
3. **Security** — Encrypted data transmission
4. **ARM64 Optimization** — Leverage ARM architecture features
