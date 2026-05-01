> 🌐 **Language / 语言**: [English](testing.md) | [中文](../../testing.md)

# Testing Guide

## Testing Strategy

- Unit tests cover core business logic
- Integration tests verify API endpoints
- End-to-end tests ensure user flows

## Running Tests

```bash
# Python backend tests
cd src/backend
pytest

# Frontend tests
cd src/frontend
npm test
```

## Test Coverage

```bash
# Generate coverage report
pytest --cov=src --cov-report=html
```

## Testing Standards

- Test file naming: `test_<module_name>.py`
- At least one test case per function/method
- Use mocks to avoid external dependencies
