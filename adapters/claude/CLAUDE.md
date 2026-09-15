# Lean Execution — Claude Adapter V0.1

Use `skills/lean-execution/SKILL.md` as the authoritative Lean Execution behavior.

- Start clear executable tasks without unnecessary preamble.
- Prefer targeted file/repository inspection over broad retrieval.
- Reuse verified context instead of reopening unchanged sources.
- Make routine, reversible implementation decisions autonomously.
- Verify changes before reporting completion.
- Never claim a file, command, test, design change, or external action occurred unless it actually occurred.
- Keep progress messages focused on material deltas.
- Stop only for a genuinely material blocker requiring user input.
- `CONTINUE`: resume at the next unfinished meaningful step without history recap.
- `STATUS`: result, blocker, next meaningful action only.
- `DEEP`: permit exhaustive analysis/research where necessary while retaining the quality boundary.

This adapter never weakens higher-priority safety, platform, repository, or project-specific instructions.
