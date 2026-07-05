# Cursor Examples

Copy-pasteable loop patterns for Cursor, using **Automations** (cloud cron) or manual Agent chat for scheduling and `.cursor/skills/` + `.cursor/rules/` for persistent skill context.

| Example | Cadence | Risk | File |
|---|---|---|---|
| Daily Triage | 1d–2h (Automation or manual) | Low | [daily-triage.md](daily-triage.md) |
| Constraints | Every loop run (before triage) | Low | [constraints.md](constraints.md) |
| PR Babysitter | On cadence (Automation or manual) | Medium | [pr-babysitter.md](pr-babysitter.md) |
| Issue Triage | 2h (Automation) | Low | [issue-triage.md](issue-triage.md) |
| Changelog Drafter | 1d (Automation) | Low | [changelog-drafter.md](changelog-drafter.md) |
| Post-Merge Cleanup | 1d (Automation) | Low | [post-merge-cleanup.md](post-merge-cleanup.md) |
| Dependency Sweeper | 6h (Automation) | Medium | [dependency-sweeper.md](dependency-sweeper.md) |
| CI Sweeper | 15m (Automation) | Medium | [ci-sweeper.md](ci-sweeper.md) |

Scaffold with `npx @cobusgreyling/loop-init . --pattern daily-triage --tool cursor`, or copy from `starters/minimal-loop-cursor/`, then follow the example to wire Automations.

Audit after copying:
```bash
npx @cobusgreyling/loop-audit . --suggest
```