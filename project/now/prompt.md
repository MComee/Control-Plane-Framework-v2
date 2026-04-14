# Active Work Prompt

You are executing the current active-work package for Control Plane Framework v2.

Required reads:
- `README.md`
- `docs/control-model.md`
- `docs/routing.md`
- `framework/rules/protected-files.md`
- `framework/rules/planning-sync.md`
- `framework/rules/execution-boundaries.md`
- `project/now/description.md`
- `project/now/metadata.json`

Allowed changes:
- files listed in `project/now/metadata.json.allowed_paths`

Forbidden changes:
- files listed in `project/now/metadata.json.forbidden_paths`

Exact update requirements:
- preserve one-project structure under `project/`
- keep priorities only in `project/docs/priorities/`
- keep evidence only in `project/evidence/`
- keep `project/now/` operational for single-tool handoff
- keep root `README.md` fully recursive and exact to tracked files

Validation requirements:
- confirm all required paths exist
- confirm forbidden paths were not changed
- confirm README tree matches tracked repository files

Evidence requirements:
- store validation output under `project/evidence/test_runs/`
- store run notes under `project/evidence/run_logs/`

Blocked-state behavior:
- if required structure cannot be preserved without violating forbidden paths, set status to `blocked` in metadata and document the blocker in `project/docs/priorities/blocked.md`.

Completion criteria:
- structure and docs are aligned
- validation evidence exists
- metadata status updated to `done`
