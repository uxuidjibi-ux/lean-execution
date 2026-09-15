# Changelog

## [0.1.1] - Unreleased

### Changed
- STATUS reports only established state, blockers, and the next action; it does not execute work or discover unrelated projects/tools.
- CONTINUE requires an established, unfinished, authorized objective before resuming.
- Missing or ambiguous objective context produces a concise blocker.
- Claude adapter delegates command semantics to the model-agnostic core.

### Added
- Good/bad command examples and reproducible command regression cases.
- Versioned Claude skill ZIP and reproducible packaging instructions.

### Validation
- Source/package checks recorded in `docs/project/TEST-LOG.md`.
- Claude behavioral retest remains pending; these changes are not yet a validated release.

## [0.1.0] - Unreleased

### Added
- Model-agnostic Lean Execution core.
- Six execution invariants.
- LEAN, DEEP, STATUS, and CONTINUE modes.
- Anti-pattern and quality-boundary references.
- Claude V0.1 adapter.
- Initial examples and evaluation framework.
