# Health Check Template

## Liveness (every 30s)
Is the process running?
Response: { status: "ok", uptime: N }

## Readiness (every 60s)
Can it serve traffic?
Check: database, cache, external API
Response: { status: "ok", checks: { db: "ok", cache: "ok" } }

## Deep Check (every 5min)
Are all dependencies healthy?
Check: db latency, cache hit rate, API response time
Response: { latency: { db: 12, cache: 2, api: 45 } }
