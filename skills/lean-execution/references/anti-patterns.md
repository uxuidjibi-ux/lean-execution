# Anti-patterns

The paired excerpts below are illustrative agent dialogue. The project’s original test log records two observed mode failures but preserves summaries only. Those observations are identified separately.

## Repeat

- **Bad agent excerpt** “I understand that you want the CSV header fixed.”
- **Good agent excerpt** “DONE: Restored the CSV header.”

## Recap

- **Bad agent excerpt** “Earlier I opened the tests and reviewed the formatter. Now I ran the regression.”
- **Good agent excerpt** “The CSV regression passes. The shared export path still needs verification.”

## Plan before action

- **Bad agent excerpt** “First I will locate the broken import, then edit it, then test.”
- **Good agent excerpt** “DONE: Fixed the import in the CI entry point. VERIFIED: The failing check now passes locally.”

## Over-retrieval

- **Bad agent excerpt** “I’ll load the full repository and all CI logs.”
- **Good agent excerpt** “The first failing step points to the Node version. I checked that step and the workflow configuration.”

## Re-inspection

- **Bad agent excerpt** “I’ll reopen all the files we already reviewed.”
- **Good agent excerpt** “The test file changed since the last run. I checked that diff and reran its test.”

## Micro-confirmation

- **Bad agent excerpt** “Should I rename the private helper now?”
- **Good agent excerpt** “DONE: Renamed the private helper and updated its callers. VERIFIED: The export tests pass.”

## Scope drift

- **Bad agent excerpt** “I also reorganized the unrelated billing module.”
- **Good agent excerpt** “DONE: Fixed the CSV formatter and retained the existing billing code.”

## Tool narration

- **Bad agent excerpt** “Running search. Opening the file. Applying my patch.”
- **Good agent excerpt** “The failure also affects scheduled exports. I’m checking that caller before closing.”

## Verbose success

- **Bad agent excerpt** “After a series of detailed steps, I am pleased to say the typo is resolved.”
- **Good agent excerpt** “DONE: Corrected the typo. VERIFIED: Checked the rendered heading.”

## Redundant output

- **Bad agent excerpt** “Here is the full contents of all three files you can already see.”
- **Good agent excerpt** “DONE: Updated the route and the two callers. VERIFIED: The targeted integration test passed.”

## Fake progress

- **Bad agent excerpt** “The migration is done. I wrote a plan.”
- **Good agent excerpt** “DONE: Drafted the migration. BLOCKED: Staging credentials are required for the dry-run.”

## Premature stop

- **Bad agent excerpt** “The patch is ready. Should I run the requested tests?”
- **Good agent excerpt** “DONE: Applied the patch. VERIFIED: The requested tests passed.”

## Observed mode failures

- **STATUS, original test T-002.** The user typed `STATUS` in a fresh session. The recorded agent behavior listed connected tools and older projects. **Good response, illustrative:** `DONE: No active objective. BLOCKED: None. NEXT: Provide the objective. VERIFIED: No task evidence in the current session.`
- **CONTINUE, original test T-003.** The user typed `CONTINUE` in a fresh session. The recorded agent behavior selected an accessible project and began work. **Good response, illustrative:** `DONE: None. BLOCKED: Active objective missing. NEXT: Provide the task or handoff. VERIFIED: No task evidence in the current session.`
