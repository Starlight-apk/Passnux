# Passnux — AI 接力棒

> 本文档专为 AI 助手设计，帮助后续 AI 快速理解项目全貌、当前进度和待办事项。

---

## 项目是什么

**Passnux**（Passion + Linux）是一个运行在 **ARM64 Linux** 上的 AI 公益服务平台。

### 核心定位

Passnux **不自研 AI 模型调用**，AI 能力全部由上游 [new-api](https://gitcode.com/QuantumNous/new-api) 网关提供。Passnux 只做四件事：

1. **前端界面** — AI 对话 Web UI
2. **API 代理** — 将 AI 请求透传转发至 new-api
3. **用户管理** — 注册、登录、Token 鉴权
4. **额度分发** — 管理用户可用额度

### 架构示意

```
用户 → [Passnux 前端] → [Passnux API 代理] → [new-api 上游网关] → [AI 模型厂商]
                              │
                    [用户管理 / 额度分发 / 对话历史]
```

---

## 技术栈（待定）

| 层级 | 候选方案 | 状态 |
|:---|:---|:---:|
| 前端框架 | React / Vue3 | 待定 |
| 前端 UI | Tailwind CSS | 待定 |
| 后端语言 | Python(FastAPI) / Node.js(Express) | 待定 |
| 数据库 | PostgreSQL | 待定 |
| 缓存 | Redis | 待定 |
| AI 网关 | **new-api**（上游，已确定） | ✅ 已确定 |
| 部署 | Debian 13 (trixie) / ARM64 | 待定 |

---

## 当前状态

- ✅ 文档框架已搭建（中英双语）
- ✅ 上游 new-api 集成方案已确定
- ❌ 无任何源代码（`src/` 目录为空）
- ❌ 无依赖管理文件（`package.json`、`requirements.txt` 等）
- ❌ 无构建/CI 配置

---

## 待办事项（按优先级）

### P0 — 基础设施
- [ ] 确定技术选型（前端 React/Vue3、后端 Python/Node.js）
- [ ] 初始化项目脚手架（`package.json` / `pyproject.toml` 等）
- [ ] 配置 `.gitignore`、`.env.example`、`docker-compose.yml`
- [ ] 搭建开发环境（数据库、Redis、new-api 本地实例）

### P1 — 核心功能
- [ ] 实现用户注册/登录（JWT 鉴权）
- [ ] 实现 API 代理层（转发至 new-api）
- [ ] 实现 AI 对话前端界面（支持流式 SSE 输出）
- [ ] 实现模型列表同步（从 new-api 获取）
- [ ] 实现额度管理（用户额度查询与扣减）

### P2 — 增强功能
- [ ] 对话历史记录（数据库持久化）
- [ ] 多模型切换 UI
- [ ] 管理后台（用户管理、额度配置）
- [ ] 国际化（i18n）前端支持

### P3 — 运维
- [ ] 编写 Dockerfile / docker-compose
- [ ] 配置 CI/CD（GitHub Actions）
- [ ] 编写单元测试与集成测试
- [ ] ARM64 兼容性验证

---

## 关键文件索引

| 文件 | 说明 |
|:---|:---|
| `README.md` | 项目简介（面向人类） |
| `ai.md` | **本文档**（面向 AI 的接力棒） |
| `LICENSE` | Passnux GPL v1.0 许可证 |
| `docs/` | 开发文档（架构/API/部署/开发规范） |
| `wiki/` | 用户文档（快速入门/功能/FAQ） |
| `docs/architecture/` | 架构设计、技术选型、目录结构 |
| `docs/api/` | API 接口文档 |
| `docs/deployment/` | 部署指南、环境变量、监控 |
| `docs/development/` | 开发环境搭建、编码规范、提交规范、测试指南 |

> 所有文档均有中英双语版本（`docs/*/i18n/en/`）。

---

## 注意事项

1. **不要直接调用 AI 模型 API** — 所有 AI 请求必须通过 new-api 转发
2. **ARM64 优先** — 所有依赖需确认 ARM64 兼容性
3. **公益免费** — 项目不设付费墙，商业部署需遵守许可证条款（10% 收入捐赠）
4. **new-api 地址** — 上游项目：[https://gitcode.com/QuantumNous/new-api](https://gitcode.com/QuantumNous/new-api)
