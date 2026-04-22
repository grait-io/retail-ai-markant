# Skills (spezialisierte Fähigkeiten)

## Was sind Skills?
Skills sind „paketiertes Wissen“ oder **spezialisierte Abläufe**, die Cursor **bei Bedarf** lädt (statt immer im Kontext zu sein).
Damit bleiben Rules schlank, und trotzdem kann man komplexe Aufgaben sauber standardisieren.

## Skills vs. Rules
- **Rules**: immer (oder dateibasiert) im Kontext → ideal für Standards/Leitplanken
- **Skills**: dynamisch/selektiv → ideal für „wie mache ich X zuverlässig?“

## Wann sind Skills sinnvoll?
- **Komplexe, wiederkehrende Aufgaben** (CI fixen, Observability-Triage, größere Refactors)
- **Agent-Loops** (iterieren bis Tests grün / UI passt)
- **Integrationen** (z.B. Jira/Confluence, Sentry, Datadog) – oft via MCP oder eigene Tools

## Wo liegen Skills?
Das ist Setup-abhängig:
- häufig in `~/.cursor/skills/` oder `~/.cursor/skills-cursor/`
- manchmal im Repo, wenn das Team Skills versionieren möchte

## Was dieses Repo schon zeigt
Im Repo sind viele „skill-ähnliche“ Automationen als `/commands` vorhanden (BMAD-Workflows), z.B.:
- [`.cursor/commands/bmad-bmm-document-project.md`](../../.cursor/commands/bmad-bmm-document-project.md)
- [`.cursor/commands/bmad-bmm-technical-research.md`](../../.cursor/commands/bmad-bmm-technical-research.md)

Diese Commands delegieren an ausführliche Workflow-Dateien unter `_bmad/` – das ist ein guter Pattern für „große“ Skills: **kurzer Einstieg → vollständiger Ablauf in canonical Dateien**.

