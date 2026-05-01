> 🌐 **Language / 语言**: [English](overview.md) | [中文](../../overview.md)

# Architecture Overview

## Overall Architecture

Passnux adopts a front-end/back-end separation architecture:

```
┌─────────────┐     ┌──────────────┐     ┌─────────────┐
│  Frontend   │────▶│  Backend API │────▶│  AI Models  │
│  (Web UI)   │◀────│  (Service)   │◀────│  (API GW)   │
└─────────────┘     └──────────────┘     └─────────────┘
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
| AI Gateway | Model request routing | TBD |

## Design Principles

1. **Modularity** — Low coupling, high cohesion
2. **Scalability** — Horizontal scaling support
3. **Security** — Encrypted data transmission
4. **ARM64 Optimization** — Leverage ARM architecture features
