# Control Plane Framework v2

Repository-native control framework for AI-assisted software development.

## Operating Intent
- Govern repository truth and execution alignment.
- Control one project per repository instance under `project/`.
- Keep planning state synchronized to repository files.
- Drive execution from `project/now/` with one-tool-at-a-time handoff.
- Validate that protected and forbidden boundaries were respected.

## Compliance Rule: Full Repository Visibility
The root `README.md` is the universal inspection entrypoint.

This file must always contain a fully recursive, exact tree of every file and every directory in this repository.

No repository paths are excluded from visibility compliance based on file type, stack, language, framework role, or subsystem role.

If any path is added, removed, renamed, moved, or reclassified, this tree must be updated in the same change set. Any mismatch is framework non-compliance.

## Repository Tree (All Paths)
```text
.
├── README.md
├── docs/
│   ├── control-model.md
│   ├── overview.md
│   ├── routing.md
│   └── start-here.md
├── framework/
│   ├── rules/
│   │   ├── execution-boundaries.md
│   │   ├── planning-sync.md
│   │   └── protected-files.md
│   └── templates/
│       ├── active-work-template.md
│       ├── feature-template.md
│       ├── task-group-template.md
│       └── task-template.md
└── project/
    ├── app/
    │   └── README.md
    ├── docs/
    │   ├── decisions.md
    │   ├── definition_of_done.md
    │   ├── execution_control.md
    │   ├── features/
    │   │   └── README.md
    │   ├── priorities/
    │   │   ├── blocked.md
    │   │   ├── done.md
    │   │   ├── later.md
    │   │   ├── next.md
    │   │   └── now.md
    │   ├── roadmap.md
    │   ├── task_groups/
    │   │   └── README.md
    │   └── tasks/
    │       └── README.md
    ├── evidence/
    │   ├── artifacts/
    │   │   └── .gitkeep
    │   ├── run_logs/
    │   │   ├── .gitkeep
    │   │   └── 2026-04-14-v2-refinement.md
    │   └── test_runs/
    │       ├── .gitkeep
    │       └── 2026-04-14-structure-validation.md
    ├── now/
    │   ├── description.md
    │   ├── metadata.json
    │   └── prompt.md
    └── vision/
        ├── brainstorming.md
        ├── constraints.md
        └── core_vision.md
```
