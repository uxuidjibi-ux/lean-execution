---
name: lean-execution
description: Use for long, multi-step agent tasks, multi-file features and refactors, debugging, failing CI, migrations, deployments, and token-heavy sessions with repeated tool use. Activate when the user requests Lean Execution or types LEAN, DEEP, STATUS, or CONTINUE as a command.
metadata:
  author: "Djibi Djigo"
  version: "2.0.0"
---

# Lean Execution

**Minimum sufficient context. Minimum necessary narration. Maximum useful execution. No quality sacrifice.**

## Activation

Apply when the task requires several dependent actions, crosses files or systems, needs investigation and verification, or resumes work with existing evidence. Activate on explicit request even for a small task. A simple standalone question usually needs only its direct answer.

Respect governing instructions, user scope, approval boundaries, and requested detail. A mode never grants permission, lowers verification, or changes the deliverable.

## Commands

Recognize the exact phrases below when sent alone or at the start of a message followed by a colon and task text. Ignore quoted examples and matching words inside ordinary prose.

| User types | Behavior |
| --- | --- |
| `LEAN` or `Use Lean Execution` | Use targeted retrieval, direct execution, and brief material updates. Default once active. |
| `DEEP` | Widen investigation and evidence when complexity, risk, or the user calls for it. Keep routine narration brief. |
| `STATUS` | Give the current outcome, verification, blocker, and next action from established state. Make no changes and initiate no broad discovery. |
| `CONTINUE` | Resume the next unfinished step in the established objective under the current execution mode. Recheck only affected or stale state. |

LEAN and DEEP persist for the current objective until switched. STATUS and CONTINUE are one-shot commands. In a fresh session, STATUS reports no active objective. CONTINUE without one requests the task or a specific handoff. Never infer a project from accessible tools or unrelated history. See [modes](references/modes.md) for combinations and edge cases.

## Execution loop

1. **Understand.** Identify the requested outcome, scope, and acceptance evidence. Use current context before retrieving more.
2. **Inspect.** Read applicable instructions and the smallest relevant source slice. Check current state before changes that could affect existing work.
3. **Execute.** Start usable work as soon as the next step is clear. Batch independent reads. Resolve reversible choices and protect unrelated changes.
4. **Verify.** Check the actual result through the normal entry point when the task requires behavioral evidence. Select the strictest applicable risk row below.
5. **Record.** Keep only material decisions, observed results, unresolved risks, and the next action. Preserve an existing handoff if the workflow calls for it.
6. **Continue.** Work through authorized next steps and recoverable failures until the requested outcome is verified or a dependency genuinely blocks it.

Avoid prompt recaps, routine tool narration, duplicate evidence, and plans that delay obvious action. Send a short update when scope, risk, evidence, or timing materially changes, and when the host or user requests one.

## Ask or proceed

| Condition | Decision |
| --- | --- |
| In scope, reversible, supported by repository convention or evidence | Proceed. Disclose an assumption if it affects the result. |
| Important fact is unknown but discoverable | Retrieve the authoritative source or reproduce the issue. Continue independent work while resolving it. |
| Irreversible, costly, or externally visible action | Confirm scope, target, and authorization from existing instructions. Prepare and verify safe steps first. Ask only for the missing material authorization or decision. |
| Material intent remains unknowable after targeted checks | Describe the consequence and ask one focused question. Leave the dependent step pending and finish independent work. |

## Verification floor

The listed checks are evidence requirements. Follow stronger project or user requirements and report any unavailable check explicitly.

| Task type | Required verification |
| --- | --- |
| Trivial copy or formatting edit | Inspect the exact diff and destination. Run a targeted lint or render check when syntax or layout can change. |
| Bug fix, refactor, or feature | Reproduce or establish baseline where practical. Run targeted behavioral tests at the affected entry point, inspect the diff, and use relevant typecheck or lint when contracts or static rules are affected. Cover callers and regression paths. |
| Database migration | Inspect constraints, lock impact, and data shape. Dry-run on representative non-production data, reconcile invariants and counts, and verify rollback or recovery strategy before a live change. |
| Auth or security | Verify allowed and denied cases, trust boundaries, and applicable cross-tenant or privilege escalation paths. Check secret handling and relevant regression coverage. |
| Payments | Use a sandbox. Verify success, failure, retries, idempotency, and applicable webhook authenticity and reconciliation. Keep evidence free of sensitive data. |
| Production deploy | Verify target, revision, preflight, health gates, and rollback path. After an authorized rollout, confirm deployed revision and health or smoke-check results. |

See [verification](references/verification-playbook.md) for check selection and [quality boundary](references/quality-boundary.md) for checks and context you must preserve.

## Completion report

Use this compact format unless the user requests another deliverable. Include concrete observed evidence and keep completed scope distinct from any pending outcome.

```text
DONE: <material result, or None>
BLOCKED: <remaining dependency and impact, or None>
NEXT: <specific next action, or None>
VERIFIED: <how checked and observed result, or what remains unverified and why>
```

Keep links or paths that help the user review the result. Distinguish observations from inferences and proposals. Claims about edits, tests, deployments, or other external state require evidence.

## Read on demand

- [Retrieval playbook](references/retrieval-playbook.md) when the next decision needs source evidence or prior evidence may be stale.
- [Anti-patterns](references/anti-patterns.md) when diagnosing repetition, scope drift, or an unwarranted stop.
- [Modes](references/modes.md), [verification](references/verification-playbook.md), and [quality boundary](references/quality-boundary.md) for their specific decisions. Load only the relevant section.
