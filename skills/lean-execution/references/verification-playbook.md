# Verification playbook

| Work | Lightest reliable evidence | Expand when |
| --- | --- | --- |
| Copy or docs | Exact diff and relevant link, render, or format lint. | Navigation or generated output changes. |
| Bug fix | Reproduction or failing regression before the fix where practical, then the same check passing after. | Multiple entry points, timing, or malformed inputs contribute. |
| Refactor or feature | Targeted tests through normal callers, diff review, and relevant typecheck or lint. | Shared contracts, package boundaries, or critical flows change. |
| CI repair | Run the failing command under the job's toolchain and inspect the workflow change. Inspect the remote run when the request includes green CI. | Services, permissions, caches, or runner differences are material. |
| UI | Inspect a targeted screenshot and exercise the changed interaction. Check affected viewport, keyboard, or error states as relevant. | Layout, focus, responsive behavior, or accessibility changes. |
| Database migration | Dry-run against representative staging data. Check lock behavior, counts, constraints, retries where relevant, and rollback or restore. | Irreversible writes or large tables require rehearsal and approved rollout conditions. |
| Auth or security | Allowed and denied requests through the protected route, including relevant cross-tenant or privilege escalation cases. Inspect redaction. | Identity, session lifecycle, or multiple trust boundaries change. |
| Payments | Sandbox success, failure, retry/duplicate events and applicable signature and ledger checks. | Live money movement, reconciliation, or provider changes are in scope. |
| Production deploy | Confirm target and revision, preflight and rollback readiness, then observe live revision and health after authorized rollout. | Canary or partial failure requires the documented hold or rollback criteria. |

A diff establishes what changed. Static checks establish the properties they test. A screenshot establishes visible state. A dry-run establishes behavior under its fixtures. Record the check, its scope, and the observed result. Escalate from narrow to wider checks when the narrow evidence cannot support the claim.
