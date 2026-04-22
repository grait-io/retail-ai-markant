# Agents (Rollen/Setups)

## Was sind „Agents“ in Cursor?
Mit „Agent“ kann zweierlei gemeint sein:
- **Agent Mode** (Arbeitsmodus): Cursor darf Tools nutzen (Suchen/Bearbeiten/Terminal).
- **Custom Agents / Agent-Profile** (Konfiguration): vordefinierte Rollen/Prompts für wiederkehrende Aufgaben (z.B. „QA“, „Architect“, „Tech Writer“).

## Wann sind Custom Agents nützlich?
- Wenn ihr wiederkehrend unterschiedliche „Hüte“ braucht (z.B. Architektur-Review vs. Test-Autor)
- Wenn ihr Menüs/Workflows anbietet (z.B. „wähle 1–6“) statt jedes Mal neu zu prompten

## Beispiel aus diesem Repo (Agent-Command Pattern)
Das Repo enthält „Agent Commands“, die eine Persona laden lassen, z.B.:
- [`.cursor/commands/bmad-agent-bmad-master.md`](../../.cursor/commands/bmad-agent-bmad-master.md)

Hier wird explizit gefordert, eine canonical Agent-Datei unter `_bmad/` zu laden. Das ist ein robustes Pattern:
**Command (kurz) → Agent-Persona/Workflow (canonical, versioniert)**.

## Versionierung / Team-Setup
Wenn ihr eigene Agent-Profile baut, ist die zentrale Frage:
- **Teamweit versionieren** (im Repo) vs. **lokal** (pro Person)

Teamweit ist sinnvoll, wenn die Agent-Rolle Teil eurer Delivery ist (z.B. ein standardisiertes Review).

