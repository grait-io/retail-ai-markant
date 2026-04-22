# MCP Servers (Model Context Protocol)

## Was ist MCP?
MCP (Model Context Protocol) ist ein Standard, um dem Agent **Tools/Integrationen** zu geben – z.B. Datenbanken, Filesystem-Zugriff oder SaaS (Jira/Confluence, etc.).
Der Agent kann damit **strukturiert** auf Daten/Operationen zugreifen, statt „irgendwie“ über Copy/Paste.

## Wo ist MCP in diesem Repo konfiguriert?
- [`.cursor/mcp.json`](../../.cursor/mcp.json)

Aktuell sind dort beispielhaft:
- ein **Postgres**-Server
- ein **Filesystem**-Server (Zugriff auf `./docs` und `./src`)

## Security: Wichtigste Leitplanken
- **Keine echten Credentials committen**.
  Die Datei enthält aktuell eine Beispiel-URL (`postgresql://user:password@...`). Für echte Projekte: per ENV/Secret-Manager.
- **Least Privilege**: Filesystem-Server nur auf die Ordner begrenzen, die wirklich nötig sind.
- **PII/Secrets**: Auch Tool-Ausgaben können sensitive Daten enthalten → Logging/Sharing beachten.

## Troubleshooting (Kurz)
- Postgres: Läuft die DB lokal? Stimmt `DATABASE_URL`?
- Filesystem: Sind die Pfade korrekt und existieren? (z.B. `./src`)
- Node/NPM: Ist `npx` verfügbar und darf Pakete laden?

