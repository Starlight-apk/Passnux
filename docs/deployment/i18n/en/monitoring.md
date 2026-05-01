> 🌐 **Language / 语言**: [English](monitoring.md) | [中文](../../monitoring.md)

# Monitoring & Alerting

## Metrics

| Metric | Description | Alert Threshold |
| :--- | :--- | :--- |
| CPU Usage | System CPU load | > 80% |
| Memory Usage | System memory usage | > 85% |
| API Response Time | Average API response time | > 5s |
| Error Rate | 5xx error ratio | > 1% |
| Model Invocations | AI request count | Custom |

## Viewing Logs

```bash
# View real-time logs
journalctl -u passnux -f

# View last 100 log entries
journalctl -u passnux -n 100
```

## Health Check

```
GET /v1/health
```

**Response:**
```json
{
  "status": "ok",
  "uptime": 3600,
  "version": "1.0.0"
}
```
