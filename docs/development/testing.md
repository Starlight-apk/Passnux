> 🌐 **语言 / Language**: [中文](testing.md) | [English](i18n/en/testing.md)

# 测试指南

## 测试策略

- 单元测试覆盖核心业务逻辑
- 集成测试验证 API 接口
- 端到端测试确保用户流程

## 运行测试

```bash
# Python 后端测试
cd src/backend
pytest

# 前端测试
cd src/frontend
npm test
```

## 测试覆盖率

```bash
# 生成覆盖率报告
pytest --cov=src --cov-report=html
```

## 测试规范

- 测试文件命名：`test_<模块名>.py`
- 每个函数/方法至少一个测试用例
- 使用 Mock 避免外部依赖