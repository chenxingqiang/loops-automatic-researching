# loop-init

Published as [`@iechor/loop-init`](https://www.npmjs.com/package/@iechor/loop-init) · [github.com/chenxingqiang/loops-automatic-researching](https://github.com/chenxingqiang/loops-automatic-researching)

Scaffold loop engineering starters into your project by pattern and tool.

**npx @iechor/loop-init . --pattern daily-triage --tool grok** works immediately.

## Install & Run

```bash
npx @iechor/loop-init . --pattern daily-triage --tool grok
npx @iechor/loop-init . --pattern daily-triage --tool opencode
npx @iechor/loop-init . --pattern daily-triage --tool cursor
npx @iechor/loop-init . --pattern daily-triage --tool trae
npx @iechor/loop-init . --pattern daily-triage --tool vscode
npx @iechor/loop-init . -p pr-babysitter -t claude
npx @iechor/loop-init . -p dependency-sweeper --dry-run
```

See [docs/RELEASE.md](../../docs/RELEASE.md) for npm publish tags. The published package bundles `starters/` and `templates/` from this monorepo.

After scaffolding, always run `npx @iechor/loop-audit . --suggest` and actually execute the first report-only loop to generate activity signals.

## Patterns

| Pattern | Default state file |
|---------|-------------------|
| `daily-triage` | `STATE.md` |
| `pr-babysitter` | `pr-babysitter-state.md` |
| `ci-sweeper` | `ci-sweeper-state.md` |
| `dependency-sweeper` | `dependency-sweeper-state.md` |
| `post-merge-cleanup` | `post-merge-state.md` |
| `changelog-drafter` | `changelog-drafter-state.md` |
| `issue-triage` | `issue-triage-state.md` |

L2 patterns (`ci-sweeper`, `dependency-sweeper`) also copy `minimal-fix` and `loop-verifier` templates when missing from the starter.

Fix-capable patterns (`pr-babysitter`, `ci-sweeper`, `dependency-sweeper`, `post-merge-cleanup`) also get a **circuit breaker**:

- `loop-guard` skill — logs each attempt to `loop-ledger.json` and runs [`loop-context`](../loop-context) `--check` before retrying
- `loop-ledger.json` — seeded with the pattern's goal and an empty `attempts` array

The breaker escalates (same error N× in a row, too many consecutive failures, token budget, or iteration cap) instead of looping in vain. Report-only patterns skip it.

Every scaffold also creates:

- `loop-budget.md` — pattern-specific daily caps and kill switch
- `loop-run-log.md` — append-only run history
- `loop-budget` skill — runtime budget guard at start/end of each run

## Tools

- `grok` (default)
- `claude`
- `codex`
- `opencode` — daily-triage ships `minimal-loop-opencode` (`skills/`, `AGENTS.md`, `opencode.json`)
- `cursor` — daily-triage ships `minimal-loop-cursor` (`.cursor/skills/`, `.cursor/agents/`)
- `trae` — daily-triage ships `minimal-loop-trae` (`.trae/skills/`)
- `vscode` — VS Code host: scaffolds `.github/skills/`, `.claude/skills/`, `.trae/skills/`, `.cline/skills/` (Copilot, Claude Code, Trae, Cline extensions)

Falls back to Grok starter paths when a per-tool variant is not yet available.

## From this repo

```bash
cd tools/loop-init && npm ci && npm test
node dist/cli.js /path/to/project --pattern daily-triage --tool grok
```

Pair with `loop-audit` and `loop-cost` after scaffolding:

```bash
npx @iechor/loop-cost --pattern daily-triage --level L1
npx @iechor/loop-audit . --suggest
```