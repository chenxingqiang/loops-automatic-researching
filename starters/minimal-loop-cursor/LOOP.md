# Loop Configuration — Minimal Triage (Cursor)

## Active Loops

| Pattern | Cadence | Status | Command |
|---------|---------|--------|---------|
| Daily Triage | 1d | L1 report-only | Cursor Automation or Agent: run `loop-triage` skill |

## Human Gates

- No auto-fix until L2 checklist complete
- All high-risk paths: human review required (see docs/safety.md denylist)

## Worktrees

- Use an isolated git worktree when drafting fixes (L2+).
- One worktree per fix attempt; discard after verifier REJECT.

## Connectors (MCP)

- MCP optional for L1 report-only loops.
- For L2+: GitHub MCP to read CI/issues; scope connectors to read + comment only until trusted.

## Scheduling

- **Week one:** Manual Agent chat with the triage prompt on your chosen cadence.
- **Unattended:** Cursor Automations (cloud cron) with the same prompt — see [examples/cursor/daily-triage.md](../../examples/cursor/daily-triage.md).

## Budget

- Max sub-agent spawns per run: 0 (L1)
- Review STATE.md daily

## Links

- Pattern: [daily-triage](../../patterns/daily-triage.md)
- Checklist: [loop-design-checklist](../../docs/loop-design-checklist.md)
