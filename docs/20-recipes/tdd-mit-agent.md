# Rezept: TDD mit Agent (rot → grün)

Ziel: Den Agent so führen, dass er **nicht „frei implementiert“**, sondern sich an Tests als Feedback-Loop hält.

## Prompt-Schablone (kopierbar)

1) **Tests zuerst (ohne Implementierung)**
Beschreibe:
- welche Datei/Funktion getestet wird (`@file`)
- erwartete Inputs/Outputs
- Edge Cases

Bitte explizit:
- Tests schreiben
- Tests ausführen und bestätigen: **FAIL**
- keine Implementierung in dieser Phase

2) **Implementierung**
Wenn Tests passen:
- Implementierung schreiben
- Tests ausführen bis **PASS**

## Repo-Anker
- Testing-Standards: [`.cursor/rules/02-testing-auto.mdc`](../../.cursor/rules/02-testing-auto.mdc)
- Command „Tests schreiben“: [`.cursor/commands/write-tests.md`](../../.cursor/commands/write-tests.md)

## Typische Fehler (und Fix)
- „Agent ändert Tests, damit es grün wird“ → explizit: **Tests dürfen nach dem Red-Commit nicht mehr verändert werden**.
- „Zu schwammige Erwartungen“ → Akzeptanzkriterien als Given/When/Then formulieren.

