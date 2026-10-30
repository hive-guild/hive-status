# HIVE Status

Prüft `https://hive-guild.de/api/health` alle zehn Minuten von außerhalb des Servers
(`.github/workflows/uptime.yml`). Ist die Seite nicht erreichbar, öffnet der Lauf ein Issue mit
dem Label `down` und schließt es wieder, sobald sie antwortet; mit dem Secret `DISCORD_WEBHOOK`
geht bei jedem Wechsel eine Zeile nach Discord. Sobald `heartbeat.txt` sechs Tage alt ist, erneuert
der nächste Lauf sie mit einem kleinen Commit; das hält den Zeitplan aktiv. Die Prüfung im Server selbst ist `hive-health` (siehe `docs/operations/deployment.md`
im Repository `hive-platform`).
