# Dependency Sweeper — Cursor (Automations / Agent)

Discover and land safe dependency updates with human gates on risky bumps.

## Scaffold

```bash
npx @cobusgreyling/loop-init . --pattern dependency-sweeper --tool cursor
```

## Automation prompt

```text
Run the dependency-triage skill. Update dependency-sweeper-state.md.
Patch-only auto-fix in worktree with loop-verifier for allowlisted packages.
Escalate major bumps, high-severity CVEs, and denylisted packages.
Max 3 attempts per package.
```

## Requirements

- `dependency-sweeper-state.md` at repo root
- Skills in `.cursor/skills/dependency-triage/` and `.cursor/agents/loop-verifier.md`

See [patterns/dependency-sweeper.md](../../patterns/dependency-sweeper.md).
