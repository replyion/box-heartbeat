# box-heartbeat

Liveness signal for the Replyion box. **No secrets. No code. No COCO usage.**

- Box cron (every 5 min) force-pushes `heartbeat/latest.json` with an ISO-8601 UTC timestamp.
- GitHub Actions (every 30 min) opens **one** issue assigned to `juangabrielarca10-arch` if the heartbeat is older than 60 minutes (box freeze / outage). Closes that issue when the heartbeat recovers.
- GitHub emails the assignee (juangabrielarca10@gmail.com via GitHub notification settings). Deduped: at most one open `box-freeze` issue per outage.

Juan approval: t1625u 19 Oct 2026 08:13 Madrid.
