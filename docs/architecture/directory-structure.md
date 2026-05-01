> 🌐 **语言 / Language**: [中文](directory-structure.md) | [English](i18n/en/directory-structure.md)

# 目录结构

## 项目文件树

```
Passnux/
├── README.md           # 项目简介
├── LICENSE             # MIT 许可证
├── docs/               # 开发文档
│   ├── index.md
│   ├── i18n/en/        # 英文翻译
│   │   └── index.md
│   ├── architecture/
│   │   ├── overview.md
│   │   ├── tech-stack.md
│   │   ├── directory-structure.md
│   │   └── i18n/en/    # 英文翻译
│   ├── development/
│   │   ├── setup.md
│   │   ├── coding-standards.md
│   │   ├── commit-convention.md
│   │   ├── testing.md
│   │   └── i18n/en/    # 英文翻译
│   ├── api/
│   │   ├── overview.md
│   │   ├── authentication.md
│   │   ├── model-inference.md
│   │   └── i18n/en/    # 英文翻译
│   └── deployment/
│       ├── deploy.md
│       ├── env-config.md
│       ├── monitoring.md
│       └── i18n/en/    # 英文翻译
├── wiki/               # 用户文档
│   ├── index.md
│   ├── i18n/en/        # 英文翻译
│   ├── quickstart/
│   │   └── i18n/en/    # 英文翻译
│   ├── features/
│   │   └── i18n/en/    # 英文翻译
│   └── faq/
│       └── i18n/en/    # 英文翻译
├── src/                # 源代码
│   ├── frontend/
│   └── backend/
└── tests/              # 测试文件
```

> 📝 标注 `src/` 和 `tests/` 为预留目录，待项目启动后填充。