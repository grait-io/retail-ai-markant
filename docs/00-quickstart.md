# Quickstart (5–10 Minuten)

## 1) Was macht Cursor hier eigentlich?
Cursor besteht (vereinfacht) aus drei Dingen:
- **Instructions**: System-Prompt + eure **Rules** (dauerhafte Leitplanken)
- **Tools**: Suchen, Dateien bearbeiten, Terminal-Befehle ausführen
- **User Messages**: eure Aufgabenbeschreibung + Nachfragen

Als Referenz liegt im Repo die offizielle Zusammenfassung: [`docs/cursor_agent_best_practices.pdf`](cursor_agent_best_practices.pdf).

## 2) Der Standard-Workflow: Plan → Execute
Wenn eine Änderung mehr als ~3 Dateien betrifft oder unklar ist:
- **Plan Mode**: Agent recherchiert, stellt Rückfragen, erstellt einen Umsetzungsplan.
- **Agent Mode**: Erst nach Plan-Freigabe wird umgesetzt.

Repo-Regel dazu: [`.cursor/rules/09-context-hygiene-always.mdc`](../.cursor/rules/09-context-hygiene-always.mdc)

## 3) Kontext richtig geben (ohne Overload)
- **Tagge gezielt**: Wenn du den Dateipfad kennst, gib ihn als `@file` an (z.B. `@src/...`).
- **Lass den Agent suchen**: Wenn du nur das Feature kennst („Auth Flow“), ist Suche oft besser als 20 Dateien zu taggen.
- **Eine Session = ein Ziel**: Wechsel des Themas → neue Konversation (reduziert Kontext-Rauschen).

## 4) Wo sind die wichtigen Template-Bausteine?
- **Rules**: `/.cursor/rules/*.mdc` (immer oder selektiv wirksam)
- **Commands**: `/.cursor/commands/*.md` (ausführbare `/commands`)
- **MCP**: `/.cursor/mcp.json` (Integrationen/Tools, z.B. Postgres, Filesystem)

## 5) Nächster Schritt
Lies als erstes die Component-Übersicht:
- [10-components/README.md](10-components/README.md)

