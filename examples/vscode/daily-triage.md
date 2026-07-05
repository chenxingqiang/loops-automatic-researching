# Daily Triage — VS Code (multi-extension)

Morning triage inside VS Code using whichever AI extension your team runs.

## Scaffold (all common paths)

```bash
npx @cobusgreyling/loop-init . --pattern daily-triage --tool vscode
```

Creates the same skills under:

- `.github/skills/` — **GitHub Copilot**
- `.claude/skills/` — **Claude Code** for VS Code
- `.trae/skills/` — **Trae** VS Code extension
- `.cline/skills/` — **Cline**

See [plugins.md](plugins.md) for Continue and other mappings.

## Agent prompt (week one — report only)

Use in Copilot Chat, Claude sidebar, Trae Agent, or Cline:

```text
Run the loop-triage skill. Read STATE.md first.
Update High Priority and Watch List only.
Do not modify source code in week one.
```

## Extension-specific notes

| Extension | Invocation tip |
|-----------|----------------|
| Copilot | Skills auto-discovered; optional `.github/copilot-instructions.md` |
| Claude Code | `$loop-triage` when skill name matches directory |
| Trae | Skill tool loads from `.trae/skills/` by description match |
| Cline | Reference skill in task prompt; skills under `.cline/skills/` |

See [patterns/daily-triage.md](../../patterns/daily-triage.md).
