# Begleitmaterialien – KI-Coding Masterclass

Dieses Repository enthält die **Begleitmaterialien** zum Workshop **„KI-Coding Masterclass“** bei **Markant**. Es dient als Arbeitsumgebung für strukturiertes, KI-gestütztes Entwickeln im Markant-Kontext.

## Präsentation

- **[Retail AI – KI-Coding Masterclass (2026)](docs/2026_RetailAI-KI-Coding%20Masterclass.pdf)** (PDF)  
  Einführung in KI-Coding, Cursor, BMAD-Methode und Best Practices. Die Folien ergänzen die praktische Arbeit mit diesem Repo.

---

## Start hier (Cursor-Doku im Repo)

Für die Nutzung dieses Templates mit Cursor gibt es eine kurze, deutschsprachige Doku unter `docs/`:
- **Index**: [docs/index.md](docs/index.md)
- **Quickstart (5–10 Minuten)**: [docs/00-quickstart.md](docs/00-quickstart.md)
- **Components (Rules/Skills/Agents/Commands/MCP/Hooks)**: [docs/10-components/README.md](docs/10-components/README.md)
- **Rezepte (TDD, Code Review)**: [docs/20-recipes/README.md](docs/20-recipes/README.md)

---

## Wichtige Ordner und Dateien

| Ordner/Datei | Beschreibung |
|--------------|--------------|
| **`.cursor/`** | Cursor-Vorlagen: **Regeln** (`.cursor/rules/`) und **Befehle** (`.cursor/commands/`). Das Team kann sie beliebig anpassen und erweitern – sie dienen als Ausgangspunkt für die Arbeit mit Cursor und BMAD. |
| **`_bmad/`** | **BMAD** (Build Method and Design): Workflows, Agenten und Konfiguration für die Phasen Analyse → Planung → Lösung → Implementierung (PRD, UX, Architektur, Sprints, Stories). |
| **`_bmad-output/`** | Generierte Artefakte: Planungsoutputs (z. B. PRDs, Briefs) und Implementierungsartefakte (Sprint-Pläne, Story-Dateien). |
| **`docs/`** | Workshop-Unterlagen, Präsentation und Projektwissen (u. a. für BMAD `project_knowledge`). |

## BMAD

Die Materialien bauen auf der **BMAD-Methode** auf. Über die Cursor-Befehle (z. B. `/bmad-help`, `/bmad-agent-bmm-analyst`) und die Inhalte in `_bmad/` arbeitet ihr mit denselben Workflows und Agenten wie in der Masterclass – von der Idee über PRD und Architektur bis zur Story-Implementierung.

## Cursor-Vorlagen (`.cursor/`)

Unter **`.cursor/`** liegen **Vorlagen** für Cursor:

- **`.cursor/rules/`** – Projektregeln (z. B. Tech-Stack, API-Design, Tests, Kontexthygiene). Sie werden von Cursor automatisch berücksichtigt.
- **`.cursor/commands/`** – Slash-Befehle für BMAD-Agenten und Workflows (z. B. Analyst, PM, Dev, PRD erstellen, Sprint-Planning).

**Diese Vorlagen könnt ihr nach Bedarf ändern, erweitern oder vereinfachen.** Sie sind als Startpunkt gedacht, nicht als feste Vorgabe.
