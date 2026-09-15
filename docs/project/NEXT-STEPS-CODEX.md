# Next Steps — Codex Handoff

## Immediate objective

Continue Lean Execution as a standalone open-source repository. Do not import unrelated CaurisPlatform context.

## Before coding

Read:
1. `docs/project/PROJECT-HANDOFF.md`
2. `docs/project/DECISIONS.md`
3. `docs/project/TEST-LOG.md`
4. `docs/project/ROADMAP.md`
5. `skills/lean-execution/SKILL.md`

## First implementation task

Prepare V0.1.1 changes to the universal core/Claude behavior:

### STATUS
When there is no active objective:
- do not enumerate connected tools;
- do not enumerate unrelated projects;
- do not retrieve broad history merely to create a status;
- return a minimal “no active objective” state.

When there is an active objective:
- report only material result/state, blocker, next action.

### CONTINUE
Before acting, establish whether an active objective exists with sufficient confidence from the current session/project/task state.

If yes:
- resume the next unfinished meaningful step.

If no:
- do not choose an unrelated project;
- return a minimal blocker requesting/identifying the missing objective context.

This check should not become a verbose planning phase.

## Evaluation requirement

Update/add eval cases before claiming the behavior is fixed.

Do not optimize only for fewer tokens. Preserve correctness, verification, safety, and explicit user intent.

## Git workflow

Use `uxuidjibi-ux/lean-execution` as source of truth.

Prefer a branch/PR for meaningful behavioral changes once normal collaborative development begins.

## Output discipline

For Codex work on this repository, apply Lean Execution itself where appropriate:

`UNDERSTAND → INSPECT → EXECUTE → VERIFY → RECORD → CONTINUE`

Report deltas, not project history.
