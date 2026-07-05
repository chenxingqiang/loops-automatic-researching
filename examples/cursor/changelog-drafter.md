# Changelog Drafter — Cursor (Automations / Agent)

Draft categorized release notes from merged PRs for human review.

## Scaffold

```bash
npx @cobusgreyling/loop-init . --pattern changelog-drafter --tool cursor
```

## Automation prompt

```text
Run changelog-scan and draft-release-notes skills on merges since last tag.
Write RELEASE_NOTES_DRAFT.md and update changelog-drafter-state.md.
Do not publish or tag releases — human review only.
Flag breaking changes and security items for explicit human approval.
```

## Requirements

- `changelog-drafter-state.md` and `RELEASE_NOTES_DRAFT.md` at repo root
- Skills scaffolded to `.cursor/skills/`

See [patterns/changelog-drafter.md](../../patterns/changelog-drafter.md).
