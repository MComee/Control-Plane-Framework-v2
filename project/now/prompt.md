# Active Work Prompt

Execute the current active-work package for Control Plane Framework v2.

Description:
Maintain v2 structure and full repository-visibility compliance without broad redesign.

Objective:
Keep repository truth stable, preserve one-project control, and enforce one-tool-at-a-time execution guidance.

Required reads:
- `README.md`
- `docs/start-here.md`
- `docs/overview.md`
- `docs/routing.md`
- `docs/control-model.md`
- `framework/rules/planning-sync.md`
- `framework/rules/execution-boundaries.md`
- `framework/rules/protected-files.md`
- `project/now/description.md`
- `project/now/metadata.json`

Allowed files:
- paths listed in the `allowed_paths` field of `project/now/metadata.json`

Forbidden files:
- paths listed in the `forbidden_paths` field of `project/now/metadata.json`

Exact update requirements:
- preserve the required `project/` architecture
- preserve a single priorities surface at `project/docs/priorities/`
- preserve a single evidence surface at `project/evidence/`
- keep `project/now/` operational for handoff
- ensure root `README.md` contains a fully recursive, exact tracked-path tree

Validation requirements:
- verify all required architecture paths exist
- verify no forbidden path was modified
- verify README tree matches tracked paths
- verify all referenced paths in docs exist

Evidence requirements:
- write run notes to `project/evidence/run_logs/`
- write validation output to `project/evidence/test_runs/`

Blocked-state instructions:
- set the `status` field in `project/now/metadata.json` to `blocked`
- document blocker in `project/docs/priorities/blocked.md`

Completion criteria:
- all required updates applied
- validation requirements passed
- evidence artifacts written
- metadata status set to `done`
