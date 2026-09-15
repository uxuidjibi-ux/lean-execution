# Lean Execution Evaluations

Compare baseline and Lean Execution runs on equivalent tasks.

Measure input tokens, output tokens, task completion, correctness, verification quality, autonomy, and regression risk.

Primary metric:
`useful_work_per_token = useful_work_score / total_tokens`

Token count alone is not success. A Lean run fails the quality gate if savings come from materially reducing correctness, required verification, safety, or explicit user requirements.

Initial task families:
1. Targeted code bug fix
2. Repository documentation update
3. Product/UX flow change
4. Evidence-based research question
5. Multi-step continuation task

## Command regressions

Run [the V0.1.1 command suite](command-regressions.md) for STATUS/CONTINUE changes. It includes fresh-session, active-objective, targeted recovery, ambiguous, completed, superseded, and blocked-task scenarios. Record actual transcripts separately from illustrative examples and static checks.
