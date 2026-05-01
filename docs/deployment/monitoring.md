> 🌐 **语言 / Language**: [中文](monitoring.md) | [English](i18n/en/monitoring.md)

# 监控告警

## 监控指标

| 指标 | 说明 | 告警阈值 |
| :--- | :--- | :--- |
| CPU 使用率 | 系统 CPU 负载 | > 80% |
| 内存使用率 | 系统内存占用 | > 85% |
| API 响应时间 | 接口平均响应 | > 5s |
| 错误率 | 5xx 错误比例 | > 1% |
| 模型调用量 | AI 请求次数（含 new-api 转发） | 自定义 |

## new-api 监控

new-api 内置了管理面板，可查看：
- 各模型调用次数与 Token 消耗
- 各 API Key 使用额度
- 请求成功率与延迟统计
- 实时日志

## 日志查看

```bash
# 查看 Passnux 实时日志
journalctl -u passnux -f

# 查看 new-api 实时日志
journalctl -u new-api -f

# 查看最近 100 条日志
journalctl -u passnux -n 100
```

## 健康检查

```
GET /v1/health
```

**响应：**
```json
{
  "status": "ok",
  "uptime": 3600,
  "version": "1.0.0"
}
```