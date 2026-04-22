# Hooks (Automationen über Events)

## Was sind Hooks?
Hooks sind Skripte, die Cursor bei bestimmten Events ausführen kann (z.B. „nachdem der Agent stoppt“).
Damit lassen sich **Feedback-Loops** bauen: „iteriere, bis ein verifizierbares Ziel erreicht ist“.

## Wofür sind Hooks besonders gut?
- **Run-until** Schleifen: „bis Tests grün“ / „bis Lint sauber“
- **Qualitätssicherung**: automatische Checks, die immer laufen sollen
- **Automatisierte Nacharbeit**: z.B. Formatierung, Zusammenfassungen, Artefakte erzeugen

## Hinweis zu diesem Repo
Aktuell gibt es hier keine versionierte Hook-Konfiguration (z.B. keine `.cursor/hooks.json`).
Die Best-Practice-Idee ist trotzdem relevant (siehe `docs/cursor_agent_best_practices.pdf`), und ihr könnt Hooks später ergänzen, wenn ein konkreter Nutzen da ist.

## Do/Don’t
- **Do**: Hook so bauen, dass er ein klares Stop-Kriterium hat.
- **Don’t**: Hooks als „magische“ Allzweck-Automation einsetzen – das erschwert Debugging.

