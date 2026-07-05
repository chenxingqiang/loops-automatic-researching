# Constraints — Trae

Binding rules your loop must never break. The `loop-constraints` skill reads `loop-constraints.md` at the start of every run.

## Quick start

```bash
mkdir -p .trae/skills/loop-constraints
cp templates/SKILL.md.loop-constraints .trae/skills/loop-constraints/SKILL.md
cp templates/loop-constraints.md loop-constraints.md
```

Optional: mirror critical rules in `.trae/rules/loop-constraints.md`:

```yaml
---
description: Loop engineering constraints — denylist and human gates
alwaysApply: true
---
```

## Before every loop run

```text
Run the loop-constraints skill. Read loop-constraints.md and enforce every rule.
Then run loop-triage. Update STATE.md (High Priority + Watch List only).
No auto-fix in week one.
```

See [docs/safety.md](../../docs/safety.md) for denylist examples.
