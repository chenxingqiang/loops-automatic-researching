# Issue Triage — Cursor (Automations / Agent)

Keep the issue queue legible. Low-risk companion to [Daily Triage](./daily-triage.md).

## Scaffold

```bash
npx @cobusgreyling/loop-init . --pattern issue-triage --tool cursor
```

## Automation prompt (week one — propose only)

```text
Run the issue-triage skill. Read issue-triage-state.md first.
Scan open issues since last run. Update state with top 5 prioritized items.
Propose labels only — do not auto-apply, close, or comment.
Escalate security and ambiguous duplicates for human review.
```

## Cadence

- 2h–1d via Cursor Automations or manual Agent chat.

See [patterns/issue-triage.md](../../patterns/issue-triage.md).
