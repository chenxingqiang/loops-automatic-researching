# Constraints — VS Code (Copilot)

```bash
npx @cobusgreyling/loop-init . --pattern daily-triage --tool vscode
# loop-constraints skill lands in .github/skills/loop-constraints/
```

Or manually:

```bash
mkdir -p .github/skills/loop-constraints
cp templates/SKILL.md.loop-constraints .github/skills/loop-constraints/SKILL.md
cp templates/loop-constraints.md loop-constraints.md
```

Run constraints before triage in Copilot Chat:

```text
Run loop-constraints skill, then loop-triage. Enforce loop-constraints.md. Report-only week one.
```
