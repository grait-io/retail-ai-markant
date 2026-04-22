# Glossar

- **Agent Harness**: Kombination aus Instructions (Prompts/Rules), Tools und User Messages, die das Agent-Verhalten bestimmt.
- **Plan Mode**: Modus, in dem der Agent recherchiert, Rückfragen stellt und einen Umsetzungsplan schreibt (ohne Änderungen).
- **Agent Mode**: Modus, in dem der Agent die Umsetzung durchführt (Dateien/Terminal), idealerweise nach einem Plan.
- **Rules**: Persistente Leitplanken/Standards (z.B. Code Style, Architektur). Liegen typ. in `.cursor/rules/`.
- **Skills**: On-demand geladenes, spezialisiertes Wissen/Automationen (z.B. „CI babysitten“, „Canvas“). Liegt je Setup lokal oder projektintern.
- **Commands**: Wiederverwendbare `/commands` als Markdown-Dateien, typ. `.cursor/commands/`.
- **MCP (Model Context Protocol)**: Standard, um dem Agent Zugriff auf Tools/Integrationen zu geben (DB, Filesystem, SaaS).
- **Hooks**: Automationen, die bei Events laufen (z.B. nach einem Agent-Stop, vor Commits, etc.).
- **Worktree**: Separater Git-Arbeitsbaum für isolierte parallele Agent-Runs.

