# Rezept: Code Review mit Agent

Ziel: Den Agent als **zweite Meinung** nutzen, ohne menschliche Review-Verantwortung abzugeben.

## Review-Setup
Gib dem Agent:
- den PR-Zweck (1–2 Sätze)
- die wichtigsten Dateien als `@file`
- „worauf achten?“ (Security, Performance, API-Contract, Tests)

## Was soll der Agent konkret liefern?
- **Findings** nach Kategorien (Bug-Risiko, Edge Cases, Security, DX)
- **konkrete Fix-Vorschläge** (welche Datei, welche Funktion)
- **Testplan** (wie verifizieren?)

## Repo-Anker
- Security-Leitplanken: [`.cursor/rules/05-security-agent.mdc`](../../.cursor/rules/05-security-agent.mdc)
- API-Konventionen: [`.cursor/rules/04-api-design-agent.mdc`](../../.cursor/rules/04-api-design-agent.mdc)
- PR-Command: [`.cursor/commands/create-pr.md`](../../.cursor/commands/create-pr.md)
- Kritischer Review-Command: [`.cursor/commands/bmad-review-adversarial-general.md`](../../.cursor/commands/bmad-review-adversarial-general.md)

## Anti-Pattern
- „Review ohne Ziel“ → ohne Kriterien liefert der Agent viel Text, wenig Signal.
- „Alles taggen“ → lieber 3 Kern-Dateien + 1 Architektur-Doc als 50 Dateien.

