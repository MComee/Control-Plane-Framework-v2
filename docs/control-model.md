# Control Model

## Layer 1: Framework self-governance
Protects framework doctrine, routing rules, protected paths, planning synchronization, and execution boundaries.

This layer defines:
- what can change
- what cannot change
- how to validate boundary compliance

## Layer 2: Single-project control
The repository controls one project under `project/`.

Governed surfaces:
- `project/vision/`
- `project/docs/features/`
- `project/docs/task_groups/`
- `project/docs/tasks/`
- `project/docs/priorities/`
- `project/docs/roadmap.md`
- `project/docs/decisions.md`
- `project/docs/definition_of_done.md`
- `project/docs/execution_control.md`
- `project/now/`
- `project/evidence/`

## Layer 3: Execution guidance
Execution is guided by repository files, not AI internals.

Execution handoff source:
- `project/now/prompt.md`

Execution must follow `project/now/metadata.json` boundaries and validation requirements.

## Non-negotiables
- repository truth is authoritative
- planning must sync to repository files
- one repo instance controls one project
- validation must confirm boundary integrity
- root `README.md` is the universal inspection surface and must remain path-accurate and fully recursive against tracked files
