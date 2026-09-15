# Lean Execution — Decision Register

## D-001 — Model agnostic core
The core must not be tied to CaurisPlatform, Figma, automotive workflows, Claude, or Codex.

## D-002 — Claude first
Validate the core behavior with Claude before building the Codex adapter.

## D-003 — GitHub source of truth
`uxuidjibi-ux/lean-execution` is the canonical public source.

## D-004 — Quality boundary
Token reduction must never come from skipping required verification, omitting material risk, guessing facts, ignoring authoritative sources, weakening safety, hiding uncertainty, claiming unperformed work, or ignoring explicit user requests.

## D-005 — Primary metric
Primary concept: **Useful work / tokens consumed**.

Supporting dimensions:
- input tokens
- output tokens
- task completion
- correctness
- verification quality
- autonomy
- regression risk

No quantitative savings claim should be published without reproducible evidence.

## D-006 — Four modes
V0.1 modes:
- LEAN
- DEEP
- STATUS
- CONTINUE

Avoid unnecessary command proliferation.

## D-007 — STATUS contract
`STATUS` should return only current material result/state, material blocker, and next meaningful action. It must not enumerate unrelated projects/tools/history.

## D-008 — CONTINUE safety
`CONTINUE` must not select an unrelated project or objective merely because one is accessible. Resume only a sufficiently established active objective. Otherwise return a concise blocker.

## D-009 — Public/open-source orientation
Lean Execution is intended for broad community use, not only the creator's projects.

## D-010 — MIT
V0.1 repository currently uses the MIT License.

## D-011 — Community claims
Market the method as an experiment/method for maximizing useful work per token until benchmarks support stronger quantitative claims.

## D-012 — Documentation
A lightweight French “Cahier des méthodologies” with screenshots is planned for community onboarding. It should be quick to read and live in the GitHub project.
