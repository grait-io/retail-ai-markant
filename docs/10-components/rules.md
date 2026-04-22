# Rules (persistente Leitplanken)

## Was sind Rules?
Rules sind **persistente Anweisungen** (Coding-Standards, Konventionen, Sicherheitsleitplanken), die Cursor dem Agent als Kontext mitgibt.
Wichtig: Rules sind kein „Wiki“ – sie sind **Arbeitsanweisungen**, die den Agent zuverlässig steuern sollen.

## Wann nutze ich Rules?
- **Wiederholte Fehler**: Wenn der Agent denselben Fehler öfter macht (z.B. falsche Ordnerstruktur).
- **Team-Standards**: Wenn Konventionen wirklich verbindlich sind (Naming, Test-Stack, Architekturpfade).
- **Security/Compliance**: Wenn bestimmte Dinge nie passieren dürfen (Secrets, Logging von PII, etc.).

## Was gehört rein (und was nicht)?
- **Gut**:
  - „Welche Commands laufen lokal/CI?“
  - „Wo liegen Specs/Docs?“ (Quelle der Wahrheit)
  - „Welche Patterns sind canonical?“ (als Dateipfad referenzieren)
- **Schlecht**:
  - komplette Styleguides (dafür linter/formatter)
  - sehr seltene Edge-Cases („falls jemals X, dann Y“) → Context Pollution

## Rule-Typen im Repo (Template-Logik)
Ihr nutzt verschiedene Rule-Arten (je nach `alwaysApply`/`globs`):
- **Always** (`alwaysApply: true`): immer aktiv
- **Auto-Attached** (`globs: ...`, `alwaysApply: false`): wird bei passenden Dateien „angeheftet“
- **Agent-requested**: wird genutzt, wenn explizit gefragt oder der Kontext es triggert

Siehe Generator/Standard: [`.cursor/rules/07-cursor-rules-meta-agent.mdc`](../../.cursor/rules/07-cursor-rules-meta-agent.mdc)

## Canonical Beispiele aus diesem Repo
- **Project Overview & Standards**: [`.cursor/rules/00-project-overview-always.mdc`](../../.cursor/rules/00-project-overview-always.mdc)
- **Context Hygiene**: [`.cursor/rules/09-context-hygiene-always.mdc`](../../.cursor/rules/09-context-hygiene-always.mdc)
- **TypeScript Standards**: [`.cursor/rules/01-typescript-auto.mdc`](../../.cursor/rules/01-typescript-auto.mdc)
- **Testing Standards**: [`.cursor/rules/02-testing-auto.mdc`](../../.cursor/rules/02-testing-auto.mdc)
- **Security Patterns**: [`.cursor/rules/05-security-agent.mdc`](../../.cursor/rules/05-security-agent.mdc)
- **Spec-driven Workflow**: [`.cursor/rules/08-spec-driven-dev-agent.mdc`](../../.cursor/rules/08-spec-driven-dev-agent.mdc)
- **API Design**: [`.cursor/rules/04-api-design-agent.mdc`](../../.cursor/rules/04-api-design-agent.mdc)

## Mini-Checkliste für gute Rules
- **Kurz und testbar**: Jede Bullet sollte „prüfbar“ sein.
- **Referenz statt Copy-Paste**: Lieber „Siehe canonical file“ als 200 Zeilen kopieren.
- **Ein Zweck pro Rule**: lieber mehrere kleine `.mdc` als ein Monolith.
- **Wenn falsch → Rule verbessern**: Wenn der Agent Mist baut, ist die Rule oft zu vage.

