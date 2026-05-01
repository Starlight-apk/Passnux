> 🌐 **Language / 语言**: [English](monitoring.md) | [中文](../../monitoring.md)

# Monitoring & Alerting

> Passnux's AI requests are actually handled by new-api, so AI-related monitoring metrics should be viewed in the new-api admin panel.

## Metrics

| Metric | Description | Alert Threshold |
| :--- | :--- | :--- |
| CPU Usage | System CPU load | > 80% |
| Memory Usage | System memory usage | > 85% |
| API Response Time | Average API response time | > 5s |
| Error Rate | 5xx error ratio | > 1% |
| Active Users | Number of active users | Custom |

## new-api Monitoring (Core AI Metrics)

new-api has a built-in admin panel for viewing all AI-related metrics:
- Model invocation counts and token consumption
- API key usage quotas
- Request success rate and latency statistics
- Real-time logs

> Passnux does not record AI invocation details itself. All AI call data is sourced from new-api.

## Viewing Logs

```bash
# View Passnux real-time logs
journalctl -u passnux -f

# View new-api real-time logs
journalctl -u new-api -f

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
