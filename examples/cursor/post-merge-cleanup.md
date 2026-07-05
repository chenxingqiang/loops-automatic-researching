# Post-Merge Cleanup — Cursor (Automations / Agent)

Follow-up tech debt and cleanup after merges to main.

## Scaffold

```bash
npx @cobusgreyling/loop-init . --pattern post-merge-cleanup --tool cursor
```

## Automation prompt (week one — report only)

```text
Run the post-merge-scan skill on merges since last run.
Update post-merge-state.md with prioritized cleanup items.
Do not modify source code in week one — report only.
Flag architectural debt for human tickets.
```

## L2 progression

- Small fixes only in isolated worktree with verifier.
- Ticket large diffs instead of auto-fixing.

See [patterns/post-merge-cleanup.md](../../patterns/post-merge-cleanup.md).
