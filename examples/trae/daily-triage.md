# Daily Triage — Trae (Agent)

Morning triage loop using Trae's Agent with project Skills in `.trae/skills/`.

Trae has no native `/loop` scheduler. Run on cadence via **Agent chat** (manual or external cron reminder) or Trae automation when available.

## Scaffold

```bash
npx @cobusgreyling/loop-init . --pattern daily-triage --tool trae
```

## Agent prompt (week one — report only)

```text
Run the loop-triage skill on the current project.
Append high-priority items to STATE.md (High Priority + Watch List only).
Do not open PRs or modify source code in week one.
Flag anything ambiguous or high-risk for human review in STATE.md.
```

## Requirements

- `STATE.md` at repo root
- `loop-triage` in `.trae/skills/loop-triage/SKILL.md`
- Optional constraints in `.trae/rules/` (see [constraints.md](constraints.md))

## Progression

- **Week one:** Report only — read `STATE.md` daily yourself.
- **L2:** Add `minimal-fix` skill + `loop-verifier` checker skill or Reviewer Agent.
- **Connectors:** GitHub MCP for CI/issues (read-only first).

See [patterns/daily-triage.md](../../patterns/daily-triage.md).
