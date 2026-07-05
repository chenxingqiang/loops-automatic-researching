# Loop Configuration — Minimal Triage (VS Code)

## Active Loops

| Pattern | Cadence | Status | Host |
|---------|---------|--------|------|
| Daily Triage | 1d | L1 report-only | VS Code AI extension (Copilot / Claude / Trae / Cline) |

## Extension layout (after `loop-init --tool vscode`)

| Extension | Skills | Optional rules |
|-----------|--------|----------------|
| GitHub Copilot | `.github/skills/` | `.github/copilot-instructions.md` |
| Claude Code | `.claude/skills/` | `AGENTS.md` |
| Trae | `.trae/skills/` | `.trae/rules/` |
| Cline | `.cline/skills/` | `.clinerules/` |

Delete paths for extensions you do not use.

## Human Gates

- No auto-fix until L2 checklist complete
- See docs/safety.md denylist

## Links

- [examples/vscode/plugins.md](../../examples/vscode/plugins.md)
- [daily-triage pattern](../../patterns/daily-triage.md)
