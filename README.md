# Lean Execution

> **Minimize unnecessary tokens, not necessary information.**

Lean Execution is an open-source, model-agnostic agent execution method designed to maximize **useful work per token** without sacrificing correctness, verification, safety, or user intent.

**Status:** v0.1.1 candidate — command contracts tightened; Claude behavioral retest pending.

## Core loop
`UNDERSTAND → INSPECT → EXECUTE → VERIFY → RECORD → CONTINUE`

## Six invariants
1. **Quality over savings** — never save tokens by reducing required correctness, safety, or verification.
2. **Action over narration** — when execution is possible, execute instead of describing execution.
3. **Minimum sufficient context** — retrieve only the context required for the current task.
4. **Verify before claiming** — never claim completion without appropriate verification.
5. **Continue unless genuinely blocked** — resolve routine, reversible decisions autonomously.
6. **Report deltas, not history** — report what changed, material blockers, and the next meaningful action.

## Modes
- `LEAN` — default.
- `DEEP` — exhaustive analysis/research when justified.
- `STATUS` — result, material blocker, next meaningful action only.
- `CONTINUE` — resume an established active objective at its next unfinished meaningful step.

## Architecture
The core is model-independent. Model-specific behavior lives in adapters.

## Evaluation
Primary metric: **Useful work / tokens consumed**.

Supporting dimensions: task completion, correctness, verification quality, autonomy, regression risk, input tokens, and output tokens.

No quantitative token-saving claim should be published until reproducible evaluations support it.

## Roadmap
1. Core V0.1
2. Claude V0.1 adapter
3. Evaluation suite
4. Public V0.1 release
5. Codex adapter

## V0.1.1 validation
- [Command examples](examples/commands.md)
- [Command regression suite](evals/command-regressions.md)
- [Claude candidate package](packages/README.md)
- [Project roadmap](docs/project/ROADMAP.md)
