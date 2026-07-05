# VS Code — AI extension path map

VS Code is a **host editor**, not a single AI product. `loop-init --tool vscode` scaffolds the same skills into the paths used by common extensions so your team can pick one (or run several side by side).

| Extension | Skills path | Rules / instructions | Verifier (checker) |
|-----------|-------------|----------------------|--------------------|
| **GitHub Copilot** | `.github/skills/<name>/SKILL.md` | `.github/copilot-instructions.md`, `.github/instructions/*.instructions.md` | `.github/skills/loop-verifier/SKILL.md` |
| **Claude Code** (VS Code) | `.claude/skills/<name>/SKILL.md` | `AGENTS.md`, `.claude/rules/` | `.claude/agents/loop-verifier.md` |
| **Trae** (VS Code) | `.trae/skills/<name>/SKILL.md` | `.trae/rules/*.md` | `.trae/skills/loop-verifier/SKILL.md` |
| **Cline** | `.cline/skills/<name>/SKILL.md` | `.clinerules/` or `.clinerules` | `.cline/skills/loop-verifier/SKILL.md` |
| **Continue.dev** | No native skills dir — embed in `config.yaml` or use `@docs` | System message in model config | Second chat pass / manual review |
| **Cursor** (separate app) | Use `--tool cursor` instead | `.cursor/rules/` | `.cursor/agents/` |

## One scaffold, many extensions

```bash
npx @cobusgreyling/loop-init . --pattern daily-triage --tool vscode
```

Writes `loop-triage` (and budget/constraints skills) to **Copilot + Claude + Trae + Cline** paths. Delete the folders for extensions you do not use.

## Pick your loop host inside VS Code

| If you primarily use… | Run loops via… | First command from `loop-init` |
|-----------------------|----------------|--------------------------------|
| Copilot Chat | Copilot panel, `@skill` or natural language | VS Code Agent (Copilot / …) prompt |
| Claude Code extension | Claude sidebar, `$loop-triage` if configured | Same — skill auto-loads from `.claude/skills/` |
| Trae extension | Trae Agent chat | Same — skill from `.trae/skills/` |
| Cline | Cline task prompt | Same — skill from `.cline/skills/` |

## Standalone apps vs VS Code plugins

- **Trae desktop / Cursor IDE** → use `--tool trae` or `--tool cursor` (single path, no multi-copy).
- **VS Code + Trae plugin** → `--tool vscode` (includes `.trae/skills/` among others).

See [VS Code Agent Skills docs](https://code.visualstudio.com/docs/copilot/customization/agent-skills) — VS Code discovers `.github/skills/`, `.claude/skills/`, and `.agents/skills/` natively.
