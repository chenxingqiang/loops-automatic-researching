# CI Sweeper — Cursor (Automations / Agent)

React to failing CI with minimal fixes. Map the loop to a **Cloud Automation** (5–15m cron) or manual Agent chat.

## Scaffold

```bash
npx @cobusgreyling/loop-init . --pattern ci-sweeper --tool cursor
```

## Automation prompt (week one — report only)

```text
Run the ci-triage skill on failing CI for main and open PRs.
Update ci-sweeper-state.md with classified failures.
Do not modify source code in week one — report only.
Escalate infra, security-test, and flake failures to human review.
```

## L2 progression

- Fix clear single-file regressions in an isolated git worktree.
- Run loop-verifier agent before proposing any fix.
- Max 3 attempts per failure; escalate after.

## Requirements

- `ci-sweeper-state.md` at repo root
- Skills in `.cursor/skills/` (scaffolded by loop-init)
- `loop-verifier` in `.cursor/agents/`

See [patterns/ci-sweeper.md](../../patterns/ci-sweeper.md).
