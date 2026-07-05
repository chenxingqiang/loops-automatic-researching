# Starters

Clone-and-run scaffolds. Copy into your project — or use `loop-init`:

```bash
npx @iechor/loop-init . --pattern daily-triage --tool grok
npx @iechor/loop-init . -p pr-babysitter -t claude
```

## Daily Triage (L1 report-only)

| Starter | Tool | Path |
|---------|------|------|
| [minimal-loop](./minimal-loop/) | Grok | `.grok/skills/` |
| [minimal-loop-claude](./minimal-loop-claude/) | Claude Code | `.claude/skills/` + `.claude/agents/` |
| [minimal-loop-codex](./minimal-loop-codex/) | Codex | `.codex/skills/` + `.codex/agents/` |
| [minimal-loop-opencode](./minimal-loop-opencode/) | Opencode | `skills/` + `AGENTS.md` |
| [minimal-loop-cursor](./minimal-loop-cursor/) | Cursor | `.cursor/skills/` + `.cursor/agents/` |
| [minimal-loop-trae](./minimal-loop-trae/) | Trae | `.trae/skills/` + `.trae/rules/` (optional) |
| [minimal-loop-vscode](./minimal-loop-vscode/) | VS Code (multi-ext) | `.github/` + `.claude/` + `.trae/` + `.cline/skills/` via `loop-init` |

## L2 assisted patterns

| Starter | Pattern | Tools | Readiness |
|---------|---------|-------|-----------|
| [pr-babysitter](./pr-babysitter/) | PR Babysitter | Grok, Claude, Codex, Cursor, Trae, VS Code | L2 assisted |
| [pr-babysitter-opencode](./pr-babysitter-opencode/) | PR Babysitter | Opencode | L1 → L2 |
| [ci-sweeper](./ci-sweeper/) | CI Sweeper | Grok, Claude, Codex, Cursor, Trae, VS Code | L2 assisted |
| [ci-sweeper-opencode](./ci-sweeper-opencode/) | CI Sweeper | Opencode | L2 cautious |
| [dependency-sweeper](./dependency-sweeper/) | Dependency Sweeper | Grok, Claude, Codex, Cursor, Trae, VS Code | L2 patch-only |
| [dependency-sweeper-opencode](./dependency-sweeper-opencode/) | Dependency Sweeper | Opencode | L2 patch-only |
| [post-merge-cleanup](./post-merge-cleanup/) | Post-Merge Cleanup | Grok, Claude, Codex, Cursor, Trae, VS Code | L1 → L2 |
| [post-merge-cleanup-opencode](./post-merge-cleanup-opencode/) | Post-Merge Cleanup | Opencode | L1 → L2 |
| [changelog-drafter](./changelog-drafter/) | Changelog Drafter | Grok, Claude, Codex, Cursor, Trae, VS Code | L1 draft → L2 |
| [changelog-drafter-opencode](./changelog-drafter-opencode/) | Changelog Drafter | Opencode | L1 draft → L2 |
| [issue-triage](./issue-triage/) | Issue Triage | Grok, Claude, Codex, Cursor, Trae, VS Code | L1 propose-only |
| [issue-triage-opencode](./issue-triage-opencode/) | Issue Triage | Opencode | L1 propose-only |

After copying:

```bash
npx @iechor/loop-audit .
npx @iechor/loop-audit . --suggest
```
