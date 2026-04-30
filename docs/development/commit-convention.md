# Git 提交规范

## 提交信息格式

```
<type>(<scope>): <subject>

<body>
```

## 类型说明

| 类型 | 说明 |
| :--- | :--- |
| `feat` | 新功能 |
| `fix` | 修复 Bug |
| `docs` | 文档更新 |
| `style` | 代码格式调整 |
| `refactor` | 代码重构 |
| `test` | 测试相关 |
| `chore` | 构建/工具链变更 |

## 示例

```
feat(api): 添加用户登录接口

实现 JWT 认证，支持用户登录并返回 token。