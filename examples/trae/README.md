# Trae Examples

Copy-pasteable loop patterns for [Trae](https://www.trae.ai/) (ByteDance AI IDE), using **Agent chat** for scheduling and `.trae/skills/` + `.trae/rules/` for persistent context.

| Example | Cadence | Risk | File |
|---|---|---|---|
| Daily Triage | 1d–2h (Agent or external cron) | Low | [daily-triage.md](daily-triage.md) |
| Constraints | Every loop run (before triage) | Low | [constraints.md](constraints.md) |
| PR Babysitter | On cadence | Medium | [pr-babysitter.md](pr-babysitter.md) |

Scaffold any pattern:

```bash
npx @cobusgreyling/loop-init . --pattern daily-triage --tool trae
```

Audit: `npx @cobusgreyling/loop-audit . --suggest`
