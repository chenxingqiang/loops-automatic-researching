# PR Babysitter — Trae (Agent)

PR watcher loop using Trae Agent + `.trae/skills/pr-review-triage/`.

## Scaffold

```bash
npx @cobusgreyling/loop-init . --pattern pr-babysitter --tool trae
```

## Agent prompt (week one — report only)

```text
Run the pr-review-triage skill on all open PRs.
Update pr-babysitter-state.md with CI status and review state.
Do not merge or push fixes in week one.
Use worktree + minimal-fix + loop-verifier only for allowlisted low-risk PRs.
Max 3 attempts per PR. No auto-merge.
```

See [patterns/pr-babysitter.md](../../patterns/pr-babysitter.md).
