> 🌐 **Language / 语言**: [English](directory-structure.md) | [中文](../../directory-structure.md)

# Directory Structure

## Project File Tree

```
Passnux/
├── README.md           # Project overview
├── LICENSE             # MIT License
├── docs/               # Development documentation
│   ├── index.md
│   ├── i18n/en/        # English translations
│   │   └── index.md
│   ├── architecture/
│   │   ├── overview.md
│   │   ├── tech-stack.md
│   │   ├── directory-structure.md
│   │   └── i18n/en/    # English translations
│   ├── development/
│   │   ├── setup.md
│   │   ├── coding-standards.md
│   │   ├── commit-convention.md
│   │   ├── testing.md
│   │   └── i18n/en/    # English translations
│   ├── api/
│   │   ├── overview.md
│   │   ├── authentication.md
│   │   ├── model-inference.md
│   │   └── i18n/en/    # English translations
│   └── deployment/
│       ├── deploy.md
│       ├── env-config.md
│       ├── monitoring.md
│       └── i18n/en/    # English translations
├── wiki/               # User documentation
│   ├── index.md
│   ├── i18n/en/        # English translations
│   ├── quickstart/
│   │   └── i18n/en/    # English translations
│   ├── features/
│   │   └── i18n/en/    # English translations
│   └── faq/
│       └── i18n/en/    # English translations
├── new-api/            # Upstream AI gateway (new-api submodule)
├── src/                # Source code
│   ├── frontend/
│   └── backend/
└── tests/              # Test files
```

> 📝 `src/` and `tests/` are reserved directories, to be populated after project launch.
