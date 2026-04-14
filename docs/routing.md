# Routing

## Operating rule
All planning and execution state must be represented in repository files. Chat-only state is non-compliant.

## Planning route
Read and update as needed:
- `project/vision/*`
- `project/docs/features/*`
- `project/docs/task_groups/*`
- `project/docs/tasks/*`
- `project/docs/priorities/*`
- `project/docs/roadmap.md`
- `project/docs/decisions.md`
- `project/docs/definition_of_done.md`
- `project/docs/execution_control.md`

## Execution route
Execution must consume `project/now/` as the handoff source:
- `project/now/description.md`
- `project/now/prompt.md`
- `project/now/metadata.json`

Execution may change only the paths explicitly allowed by the active-work package.

## Validation route
Validation must confirm:
- protected and restricted boundaries were respected
- required validation checks ran
- required evidence was written under `project/evidence/`

## Repository visibility compliance
The root `README.md` file tree is a required control surface. It must be fully recursive and exactly match the tracked repository state.
