# Components – Überblick

Dieses Template nutzt mehrere Cursor-Bausteine. Die Faustregel:
- **Rules** = dauerhaftes „Policy/Standards“-Gedächtnis (klein halten)
- **Skills** = bei Bedarf geladenes „Wie mache ich X?“-Wissen (dynamisch)
- **Agents** = vordefinierte Rollen/Prompts (für wiederkehrende Arbeitsweisen)
- **Commands** = wiederholbare `/commands` (Checklisten + Automationsschritte)
- **MCP Servers** = Integrationen (DB, Filesystem, SaaS) über Model Context Protocol
- **Hooks** = Automationen, die bei Events laufen (z.B. „loop until tests pass“)

## Kurzmatrix

| Component | Wofür? | Wo im Repo? |
|---|---|---|
| Rules | Coding-Standards, Architektur-Konventionen, Sicherheitsleitplanken | `.cursor/rules/` |
| Skills | komplexe, spezialisierte Fähigkeiten (on-demand) | i.d.R. `~/.cursor/skills*` oder projektintern (Setup-abhängig) |
| Agents | wiederverwendbare Agent-Personas/Setups | Setup-abhängig (oft Cursor UI/Profiles) |
| Commands | wiederholbare Abläufe als `/command` | `.cursor/commands/` |
| MCP Servers | Tooling/Integrationen (z.B. Postgres) | `.cursor/mcp.json` |
| Hooks | Event-getriggerte Automationen | typ. `.cursor/hooks.json` + Skripte |

## Deep Dives
- [Rules](rules.md)
- [Skills](skills.md)
- [Agents](agents.md)
- [Commands](commands.md)
- [MCP Servers](mcp-servers.md)
- [Hooks](hooks.md)

