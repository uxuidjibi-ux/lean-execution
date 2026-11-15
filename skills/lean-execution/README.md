# Lean Execution v2.0

Long agent sessions accumulate repeated context, routine narration, and pauses for reversible choices. Lean Execution gives agents a repeatable workflow for retrieving evidence, advancing work, and verifying outcomes at a depth appropriate to the risk.

**Author** Djibi Djigo — Product & CX Strategist | UX/UI, AI Workflows & Branding.

## What is inside

- `SKILL.md` with the execution loop, four commands, risk matrix, and completion report.
- `references/` with quality, retrieval, verification, mode, and anti-pattern guidance.
- `templates/` with persistent project instructions and a one-line session starter.
- `evals/` with ten scenarios, a paired benchmark worksheet, and [preflight results](evals/preflight-results.md).
- `examples/` with three illustrative before-and-after transcripts.

## 30-second install

Extract the package so the folder is named `lean-execution` and contains `SKILL.md` directly. Copy that folder into the applicable project directory, open a new agent session in the project, then send `Use Lean Execution: <your task>`. If discovery is unavailable in your version or surface, paste the matching persistence template into your project instructions and point it at the extracted skill.

| Agent | Copy into | Optional persistent instructions |
| --- | --- | --- |
| Claude Code | `.claude/skills/` | Merge [CLAUDE.md](templates/CLAUDE.md) into project `CLAUDE.md`. |
| Cursor | `.cursor/skills/` | Copy the [modern rule](templates/cursor-rule.mdc) to `.cursor/rules/lean-execution.mdc`, or paste the [legacy snippet](templates/cursorrules.txt) into `.cursorrules` where supported. |
| Codex CLI | `.agents/skills/` | Merge [AGENTS.md](templates/AGENTS.md) into project `AGENTS.md`. |
| GitHub Copilot | `.github/skills/` | Merge the [Copilot block](templates/copilot-instructions.md) into `.github/copilot-instructions.md` on a surface that supports it. |
| Gemini CLI | `.gemini/skills/` | Merge [GEMINI.md](templates/GEMINI.md) into project `GEMINI.md`. |

Use a client version with native Agent Skills support for discovery. Preserve existing project instructions. The [session starter](templates/session-starter.txt) is also available for one-off sessions.

Installation references for the [Agent Skills specification](https://agentskills.io/specification), [Claude Code](https://code.claude.com/docs/en/skills), [Cursor](https://cursor.com/docs/skills), [Codex CLI](https://developers.openai.com/codex/skills), [Copilot](https://docs.github.com/en/copilot/concepts/customizations/agent-skills), and [Gemini CLI](https://geminicli.com/docs/cli/skills/).

## Modes

| Command | Use |
| --- | --- |
| `LEAN` | Execute with targeted context and brief updates. |
| `DEEP` | Widen analysis and gather more evidence. |
| `STATUS` | Report the established state without changes. |
| `CONTINUE` | Resume the next unfinished step of a known objective. |

## FAQ

**Does it reduce quality?** It preserves explicit requirements, material risks, evidence, and risk-based verification. The included benchmark lets you measure quality and efficiency for your own tasks.

**Does it skip tests?** Required tests still run. A trivial copy change may need only a diff and render check. Sensitive work needs behavioral evidence.

**Does it work with Cursor?** Use native Agent Skills on a supported Cursor version, or use the project-rule template to load the skill and retain its core behavior.

## Changelog

### v2.0.0

- Defined exact commands, fresh-session behavior, and resume criteria.
- Added risk-based verification, a four-field report, and on-demand playbooks.
- Added five agent setup paths, ten evaluation scenarios, a benchmark protocol, and illustrative transcripts.
