# Loop Configuration — Minimal Triage (Trae)

## Active Loops

| Pattern | Cadence | Status | Command |
|---------|---------|--------|---------|
| Daily Triage | 1d | L1 report-only | Trae Agent: run `loop-triage` skill |

## Human Gates

- No auto-fix until L2 checklist complete
- All high-risk paths: human review required (see docs/safety.md denylist)

## Worktrees

- Use an isolated git worktree when drafting fixes (L2+).
- One worktree per fix attempt; discard after loop-verifier REJECT.

## Rules & Skills

- Skills: `.trae/skills/<name>/SKILL.md` (on demand)
- Rules: `.trae/rules/*.md` (always-on constraints — optional)
- Verifier: `.trae/skills/loop-verifier/SKILL.md` or a dedicated Reviewer Agent in Trae settings

## Scheduling

- **Week one:** Manual Agent chat with the triage prompt on your chosen cadence.
- **Unattended:** External cron + Trae CLI/API if available, or reminder workflow — see [examples/trae/daily-triage.md](../../examples/trae/daily-triage.md).

## Budget

- Max sub-agent spawns per run: 0 (L1)
- Review STATE.md daily

## Links

- Pattern: [daily-triage](../../patterns/daily-triage.md)
- Checklist: [loop-design-checklist](../../docs/loop-design-checklist.md)
