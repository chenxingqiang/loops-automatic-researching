# VS Code Examples (multi-extension host)

VS Code runs many AI agents as **extensions** — Copilot, Claude Code, Trae, Cline, Continue, and more. Same loop shape; different skill folders.

| Example | Cadence | Risk | File |
|---|---|---|---|
| Daily Triage | 1d (extension chat) | Low | [daily-triage.md](daily-triage.md) |
| Extension paths | — | — | [plugins.md](plugins.md) |
| Constraints | Before each run | Low | [constraints.md](constraints.md) |
| PR Babysitter | On cadence | Medium | [pr-babysitter.md](pr-babysitter.md) |

```bash
npx @cobusgreyling/loop-init . --pattern daily-triage --tool vscode
```

Scaffolds skills to `.github/skills/`, `.claude/skills/`, `.trae/skills/`, and `.cline/skills/` — remove paths for extensions you do not use.

**Not VS Code:** Cursor and Trae **standalone IDEs** → `--tool cursor` or `--tool trae` instead.
