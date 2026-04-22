# Commands (`/commands`)

## Was sind Commands?
Commands sind **Agent-ausführbare** Markdown-Dateien, die als `/command` in Cursor verfügbar sind.
Sie eignen sich für Checklisten und wiederholbare Abläufe, die „immer gleich“ laufen sollen.

## Wo liegen Commands?
In diesem Repo: [`.cursor/commands/`](../../.cursor/commands/)

## Gute Commands sind…
- **deterministisch** (klare Schritte, klare Reihenfolge)
- **sicher** (keine gefährlichen Defaults wie Force-Push)
- **verifizierbar** (Tests/Lint/Build als Ziel)
- **kurz**: Details liegen besser in canonical Dateien (z.B. Workflows unter `_bmad/`)

## Canonical Beispiele aus diesem Repo
- PR erstellen: [`.cursor/commands/create-pr.md`](../../.cursor/commands/create-pr.md)
- Tests generieren: [`.cursor/commands/write-tests.md`](../../.cursor/commands/write-tests.md)
- Projekt-/CI-Konvention (hier als „Skill“): [`.cursor/commands/mr.md`](../../.cursor/commands/mr.md)

## BMAD-Commands als „Workflow Wrapper“
Viele `bmad-*` Commands im Repo sind Wrapper, die eine ausführliche canonical Datei laden. Beispiele:
- [`.cursor/commands/bmad-help.md`](../../.cursor/commands/bmad-help.md)
- [`.cursor/commands/bmad-party-mode.md`](../../.cursor/commands/bmad-party-mode.md)

Das ist nützlich, wenn ihr umfangreiche Prozesse habt: Command bleibt kurz, die Details leben versioniert im Workflow.

