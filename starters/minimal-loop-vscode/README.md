# Minimal Loop Starter — VS Code (multi-extension)

Report-only daily triage (L1) for VS Code AI extensions.

```bash
npx @cobusgreyling/loop-init . --pattern daily-triage --tool vscode
```

`loop-init` copies skills to **Copilot, Claude Code, Trae, and Cline** paths. Remove unused folders after scaffold.

## Manual copy (Copilot only)

```bash
cp -r starters/minimal-loop-vscode/.github/skills/loop-triage .github/skills/
cp -r starters/minimal-loop-vscode/.github/skills/loop-verifier .github/skills/
cp starters/minimal-loop-vscode/STATE.md.example STATE.md
```

For other extensions see [examples/vscode/plugins.md](../../examples/vscode/plugins.md).

## First loop

```text
Run the loop-triage skill. Read STATE.md first.
Update High Priority and Watch List only.
Do not modify source code in week one.
```
