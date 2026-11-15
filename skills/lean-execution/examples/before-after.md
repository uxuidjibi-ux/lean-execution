# Before and after

All three transcript pairs are illustrative. Tool actions and results describe fictional fixtures.

## 1. CSV regression

**Same user prompt:** “Fix duplicate CSV headers in scheduled exports.”

**Without the skill**

> Agent: I’ll investigate the export system, read its files, and plan a patch.
>
> Agent: I found the shared writer and made the change. Would you like me to run the export tests?

**With the skill**

> Agent: DONE: Scheduled exports write one header.
>
> BLOCKED: None.
>
> NEXT: None.
>
> VERIFIED: The scheduled-export regression failed before the patch and passed after it. Reviewed the shared writer diff.

## 2. Migration dependency

**Same user prompt:** “Prepare a non-null customer status migration. The database already has legacy rows.”

**Without the skill**

> Agent: I’ll assign a default so we can add the constraint. The migration is ready.

**With the skill**

> Agent: DONE: Identified the affected legacy rows and drafted checks for the constraint rollout.
>
> BLOCKED: The backfill value controls customer access and no rule is documented.
>
> NEXT: Confirm the policy for legacy accounts.
>
> VERIFIED: Inspected the schema and staging fixture counts. Dry-run pending the backfill decision.

## 3. CI repair

**Same user prompt:** “Fix failing CI using the attached test log.”

**Without the skill**

> Agent: I’ll read the full logs and check every job.
>
> Agent: I updated the Node setup. CI is fixed.

**With the skill**

> Agent: DONE: Matched the CI Node version to the project’s pinned version.
>
> BLOCKED: No access to the hosted runner from this checkout.
>
> NEXT: Rerun the hosted job.
>
> VERIFIED: The failing command passed locally on the pinned toolchain. Hosted CI remains unverified.
