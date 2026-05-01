> 🌐 **语言 / Language**: [中文](coding-standards.md) | [English](i18n/en/coding-standards.md)

# 编码规范

## 通用原则

- 代码可读性优先于技巧性
- 遵循语言社区公认的最佳实践
- 保持一致的代码风格

## Python 规范

- 遵循 PEP 8 编码规范
- 使用 4 空格缩进
- 行长度不超过 88 字符
- 使用类型注解 (Type Hints)

## JavaScript / TypeScript 规范

- 使用 2 空格缩进
- 优先使用 const / let，避免 var
- 使用 ES6+ 语法
- 推荐使用 TypeScript

## 命名规范

| 类型 | 规范 | 示例 |
| :--- | :--- | :--- |
| 类名 | PascalCase | `UserService` |
| 函数/方法 | camelCase | `getUserById()` |
| 变量 | snake_case (Python) / camelCase (JS) | |
| 常量 | UPPER_SNAKE_CASE | `MAX_RETRY_COUNT` |
| 文件 | snake_case | `user_model.py` |