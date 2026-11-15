# Paired benchmark

1. Pick a task from [tasks.md](tasks.md). Record fixture revision, starting state, acceptance checks, limits, and any seeded blockers. Use disposable copies.
2. Compare the same agent, model, settings, tools, permission policy, and objective in two fresh sessions. Disable Lean Execution and its adapters for baseline. Enable only the skill for the treatment. Send identical task text, including mode words if the scenario tests them.
3. Predefine the stop condition and answer any clarification with the same scripted facts. Alternate ordering across repeat pairs and reset the fixture between runs. Never carry history or evidence from one run into the other.
4. Save redacted run IDs, transcript/tool evidence, final diff, and evaluator check output. Count every user and assistant conversational turn through the stopping point. Track tool calls separately. Sum input/output tokens from provider usage for all model requests including skill overhead. Record cached tokens separately when available and follow the provider’s definition. Mark missing metrics as unavailable.
5. Run independent acceptance checks against both outputs. Score the shared and case-specific checklists. Compare efficiency for pairs where both pass. Report failures, blocked runs, and missing metrics separately.

| Pair / case | Condition | Agent / model / revision | Input tokens | Cached input | Output tokens | User turns | Assistant turns | Tool calls | Quality pass / fail | Evidence |
| --- | --- | --- | ---: | ---: | ---: | ---: | ---: | ---: | --- | --- |
| | Baseline | | | | | | | | | |
| | Lean Execution | | | | | | | | | |

Report the difference as Lean minus baseline for each available metric. Share underlying counts and sample size. Keep benchmark claims limited to measured tasks and environments.
