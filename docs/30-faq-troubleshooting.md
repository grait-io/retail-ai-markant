# FAQ & Troubleshooting

## Der Agent „driftet“ (macht etwas anderes als gewünscht)
- Formuliere das Ziel als **verifizierbares Ergebnis** (Tests, Build, konkrete Ausgabe).
- Bitte zuerst um einen **Plan** (Plan Mode) und korrigiere den Plan, statt im Run zu „patchen“.
- Reduziere Kontext: Tagge nur die 1–3 wichtigsten Dateien statt ganzer Ordner.

## Der Agent findet die richtige Datei nicht
- Tagge den Pfad explizit als `@file`.
- Gib Suchbegriffe/Signaturen („Funktion `createOrder`“, „Route `/api/users`“).

## Rules „fühlen sich zu groß“ an
Rules sind immer Kontext. Halte sie klein und füge nur hinzu, was wiederholt schiefgeht.
Siehe: [`.cursor/rules/09-context-hygiene-always.mdc`](../.cursor/rules/09-context-hygiene-always.mdc)

## `/commands` sind zu vage / führen zu falschen Schritten
- Commands sollten **deterministisch** sein: klare Schritte, klare Erwartungen.
- Gute Beispiele im Repo: [`.cursor/commands/create-pr.md`](../.cursor/commands/create-pr.md), [`.cursor/commands/write-tests.md`](../.cursor/commands/write-tests.md)

## MCP verbindet nicht / Tooling „geht nicht“
Typische Ursachen:
- falsche ENV/URL (z.B. `DATABASE_URL`)
- fehlende lokale Services (z.B. Postgres läuft nicht)
- falsche Pfade/Permissions beim Filesystem-Server

Repo-Konfig: [`.cursor/mcp.json`](../.cursor/mcp.json)

