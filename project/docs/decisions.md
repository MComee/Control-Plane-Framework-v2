# Decisions

## DEC-001
Decision: this repository governs repository truth and execution alignment, not AI internals.

Impact:
- control remains file-centric
- execution remains tool-agnostic
- validation remains boundary-centric

## DEC-002
Decision: one repository instance controls one project under `project/`.

Impact:
- no multi-project routing in this repository
- all planning state remains under `project/docs/` and `project/vision/`

## DEC-003
Decision: execution handoff source is `project/now/`, with `project/now/prompt.md` as the executable prompt surface.

Impact:
- execution context is explicit and reproducible
- active-work boundaries are enforceable

## DEC-004
Decision: root `README.md` must remain a fully recursive, exact mirror of tracked repository paths.

Impact:
- visibility stays deterministic for humans and tools
- path drift is treated as framework non-compliance
