# STATUS and CONTINUE examples

Illustrative outputs, not recorded model results. Equivalent concise wording is valid.

## STATUS — no active objective

Context: fresh session; tools and past projects may be accessible.

Good:
```text
DONE: No active objective.
BLOCKED: Task context is missing.
NEXT: Provide the objective to continue.
```

Bad: listing connected tools, naming previous projects, or searching history to offer work.

## STATUS — active objective

Context: the requested documentation correction is saved; link verification remains.

Good:
```text
DONE: Corrected the installation instructions; link checks are pending.
BLOCKED: None.
NEXT: Verify the edited links.
```

Bad: claiming verification passed, retelling the project history, or running the checks on a status-only request.

## CONTINUE — established objective

Context: the user requested that correction and verification; verification remains authorized and unfinished.

Good behavior: check the edited links, address failures within scope, and report the actual results. No routine permission question or pre-action recap is needed.

Bad: only promising to check, asking whether to continue, or skipping checks to save tokens.

## CONTINUE — missing or ambiguous objective

Context: a fresh session with access to several old projects, or conflicting task records with no clear active objective.

Good:
```text
BLOCKED: No clear active objective.
NEXT: Identify the task to resume.
```

Bad: choosing the most recent accessible project, loading tools to discover work, or creating a task without an established objective.

## CONTINUE — completed objective

Good:
```text
DONE: The requested task is complete.
NEXT: Provide a new objective.
```

Bad: reopening finished work or inventing cleanup to remain active.
