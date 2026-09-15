# Lean Execution — Roadmap

## V0.1 — Current
- Model-agnostic core.
- Six invariants.
- Anti-pattern reference.
- Quality boundary.
- Claude adapter.
- Examples.
- Evaluation template.
- Public GitHub repository.
- Global Claude installation tested.

## V0.1.1 — Tighten Claude behavior
- Strengthen STATUS output contract.
- Add active-objective confidence rule for CONTINUE.
- Reduce blocker verbosity.
- Add explicit “do not enumerate unrelated projects/tools” rule.
- Add examples of good/bad STATUS and CONTINUE behavior.
- Repackage Claude skill.
- Retest.

## V0.2 — Evaluation
- Build reproducible baseline-vs-Lean test set.
- Capture input/output token counts where available.
- Define useful-work scoring rubric.
- Establish quality gate.
- Publish first transparent results, including failures.

## Community documentation
- Publish `docs/Cahier-des-methodologies.pdf`.
- Include real screenshots of GitHub setup, Claude Customize/Skills upload, installed skill, STATUS test, and CONTINUE behavior.
- Add a 60-second Quick Start Markdown.
- Add downloadable Claude skill package or release asset.
- Add community evaluation contribution workflow.

## Codex
After Claude/core tightening:
- design Codex adapter without duplicating the core;
- use repository instructions appropriately;
- test equivalent cases;
- compare Claude vs Codex adapter behavior.

## Later
- additional agent adapters where appropriate;
- community-submitted evals;
- optional lightweight evaluation utility;
- social launch assets and public beta release.
