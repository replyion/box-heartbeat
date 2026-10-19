# box-heartbeat

Liveness signal for the Replyion box. **No secrets. No code. No COCO usage.**

- Box cron (every 5 min) force-pushes `heartbeat/latest.json` on branch **`live`**.
- GitHub Actions (every 30 min, from `main`) opens **one** issue assigned to `juangabrielarca10-arch` if the heartbeat is older than 60 minutes. Closes it when the heartbeat recovers.
- GitHub emails the assignee (configure juangabrielarca10@gmail.com on that GitHub account). Deduped: at most one open `box-freeze` issue per outage.

Juan approval: t1625u 19 Oct 2026 08:13 Madrid.
