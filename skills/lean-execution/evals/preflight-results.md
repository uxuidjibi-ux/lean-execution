# v2.0 preflight results

Recorded November 14, 2026, before final archive validation. These are package checks and startup attempts. The [paired benchmark](benchmark.md) has no measurements.

| Test | Method | Observed result |
| --- | --- | --- |
| Package smoke check | Checked the required files, parsed YAML, checked the line budget, resolved relative links, and counted the scenarios and transcript pairs. | PASS. An 84-line SKILL.md, ten scenarios, and three illustrative transcript pairs. |
| Negative control | Removed `references/modes.md` from a disposable package copy and ran the same checker. | PASS. The checker rejected the copy and identified the exact missing path. |
| Codex CLI start, fresh CONTINUE and STATUS | Invoked Codex CLI 0.167.0-alpha.4 separately in an isolated project with the native skill path, read-only tool sandbox, and ephemeral sessions. Retried CONTINUE with workspace-local SQLite state. | BLOCKED. The app-server client failed to initialize with `Read-only file system (os error 30)`. No agent response was observed. |

Observed output from the package smoke check and negative control:

```text
PASS required package files
PASS frontmatter and line budget
PASS relative links
PASS evaluation and transcript inventory
AssertionError: Missing: ['references/modes.md']
```

To repeat the structure portion, validate SKILL.md against the Agent Skills schema, verify each local Markdown link and the inventory in the buyer guide, then repeat on a disposable copy with `references/modes.md` removed and confirm rejection. To evaluate runtime behavior, run [E10 in the task suite](tasks.md) on an agent host that can start a fresh session. Use the [benchmark](benchmark.md) for a baseline comparison.
