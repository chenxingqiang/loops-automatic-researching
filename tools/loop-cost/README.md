# loop-cost

Estimate daily token spend for [loop engineering](https://github.com/chenxingqiang/loops-automatic-researching) patterns by cadence and readiness level (L1–L3).

Uses cost metadata from `patterns/registry.yaml`.

Published as [`@iechor/loop-cost`](https://www.npmjs.com/package/@iechor/loop-cost).

## Install & Run

```bash
npx @iechor/loop-cost --pattern ci-sweeper --cadence 15m --level L2
npx @iechor/loop-cost --pattern daily-triage --level L1 --json
npx @iechor/loop-cost --list
```

**From this repo:**

```bash
cd tools/loop-cost
npm install
npm test
```

## Options

| Flag | Description |
|------|-------------|
| `--pattern` | Pattern id (see `--list`) |
| `--cadence` | Override cadence (e.g. `15m`, `1d`) |
| `--level` | `L1`, `L2`, or `L3` (default `L1`) |
| `--conservative` | Use slower cadence from ranges |
| `--json` | Machine-readable output |

## Scenarios

Each estimate includes:

- **Early-exit / no-op** — empty watchlist, minimal tokens
- **Full triage** — every run does a full scan
- **Action every run** — implementer + verifier every time (worst case)
- **Realistic blend** — level-based mix (documented in output)

Pair with `loop-budget.md` (scaffolded by `loop-init`) and `loop-audit` cost observability checks.

See [docs/operating-loops.md](../../docs/operating-loops.md).