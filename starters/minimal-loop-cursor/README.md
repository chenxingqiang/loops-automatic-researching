# Minimal Loop Starter — Cursor

Clone this into your project root to run a **report-only daily triage loop** (L1 readiness).

Or scaffold automatically:

```bash
npx @cobusgreyling/loop-init . --pattern daily-triage --tool cursor
```

## Quick Start (manual copy)

1. Copy files into your repo:

   ```bash
   cp -r starters/minimal-loop-cursor/.cursor/skills/loop-triage .cursor/skills/
   cp starters/minimal-loop-cursor/.cursor/agents/loop-verifier.md .cursor/agents/
   cp starters/minimal-loop-cursor/STATE.md.example STATE.md
   cp starters/minimal-loop-cursor/LOOP.md .
   ```

2. Customize `STATE.md` project name.

3. Start the loop (Cursor Agent or Automation):

   ```text
   Run the loop-triage skill on the current project.
   Read STATE.md first. Update High Priority and Watch List only.
   Do not open PRs or modify source code in week one.
   ```

4. Read `STATE.md` each morning for 1–2 weeks. Tune the triage skill.

5. When triage quality is good, add `minimal-fix` from `templates/SKILL.md.minimal-fix` and enable small auto-wins with the verifier agent in an isolated worktree.

## What's Included

| File | Purpose |
|------|---------|
| `STATE.md.example` | State spine template |
| `.cursor/skills/loop-triage/SKILL.md` | Triage skill |
| `.cursor/agents/loop-verifier.md` | Checker sub-agent for L2+ |
| `LOOP.md` | Loop config doc for your team |

## Next Steps

- [Loop Design Checklist](../../docs/loop-design-checklist.md)
- [Daily Triage pattern](../../patterns/daily-triage.md)
- [Cursor example](../../examples/cursor/daily-triage.md)
- Run `npx @cobusgreyling/loop-audit .` for readiness score
