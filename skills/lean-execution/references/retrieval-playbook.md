# Retrieval playbook

1. **Start with the decision.** State internally what evidence would change the next action. Reuse observations and exact paths already available for the current revision.
2. **Search before reading.** Use `rg --files` to identify candidates and `rg -n 'symbol|error' src tests` to locate the relevant lines. Use the host's search when a shell is unavailable and grep when ripgrep is unavailable.
3. **Read bounded ranges.** Open the matching function, neighboring constraints, and direct callers. For example, `sed -n '120,170p' src/checkout.ts`. Expand when contracts, side effects, or acceptance criteria require it.
4. **Follow the boundary.** Locate applicable repository instructions, tests, runtime configuration, and authoritative external contracts only where they affect the change. For CI, start with the first causal error and the matching job or step.
5. **Retain compact evidence.** Keep the source path, revision or run ID when relevant, result, and remaining uncertainty. Batch independent reads and reuse prior tool output.
6. **Refresh on a reason.** Reopen only affected slices when files, branch, environment, or assumptions change, or when new evidence contradicts an earlier result. An old result for a changed revision is historical evidence.

Prefer a small query with an explicit target to recursive dumps. Avoid rerunning a full suite solely to reproduce output already recorded for the same revision and environment.
