# Minimal Loop Starter — Trae

Clone this into your project root to run a **report-only daily triage loop** (L1 readiness).

Or scaffold automatically:

```bash
npx @cobusgreyling/loop-init . --pattern daily-triage --tool trae
```

## Quick Start (manual copy)

```bash
cp -r starters/minimal-loop-trae/.trae/skills/loop-triage .trae/skills/
cp -r starters/minimal-loop-trae/.trae/skills/loop-verifier .trae/skills/
cp starters/minimal-loop-trae/STATE.md.example STATE.md
cp starters/minimal-loop-trae/LOOP.md .
```

## First loop (Trae Agent)

```text
Run the loop-triage skill on the current project.
Read STATE.md first. Update High Priority and Watch List only.
Do not open PRs or modify source code in week one.
```

See [examples/trae/daily-triage.md](../../examples/trae/daily-triage.md).
