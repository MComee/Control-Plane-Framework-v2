# Control Plane Framework v2

## Purpose
This repository is a repository-native control framework for AI-assisted software development.

It governs repository truth and execution alignment. It does not govern AI internals.

One repository instance controls one project under `project/`.

## Control Commitments
- Preserve framework integrity and doctrine.
- Preserve one controlled project and its vision.
- Preserve decomposition into features, task groups, and tasks.
- Preserve explicit priorities and current active-work state.
- Guide one chosen tool at a time through `project/now/` handoff.
- Keep repository truth stable so different tools can execute against the same controlled state.

## Operating Model
1. Planning must synchronize to repository files.
2. Execution must consume `project/now/`.
3. Validation must confirm protected boundaries were respected.
4. Evidence must be written under `project/evidence/`.

## Repository Visibility Rule
`README.md` must contain a fully recursive, exact tree of tracked files and tracked directories. Any tracked path change requires updating this tree in the same change set.

## Tracked Repository Tree
```text
README.md
docs/
  control-model.md
  overview.md
  routing.md
  start-here.md
framework/
  rules/
    execution-boundaries.md
    planning-sync.md
    protected-files.md
  templates/
    active-work-template.md
    feature-template.md
    task-group-template.md
    task-template.md
project/
  app/
    README.md
  docs/
    decisions.md
    definition_of_done.md
    execution_control.md
    features/
      README.md
    priorities/
      blocked.md
      done.md
      later.md
      next.md
      now.md
    roadmap.md
    task_groups/
      README.md
    tasks/
      README.md
  evidence/
    artifacts/
      .gitkeep
    run_logs/
      .gitkeep
    test_runs/
      .gitkeep
  now/
    description.md
    metadata.json
    prompt.md
  vision/
    brainstorming.md
    constraints.md
    core_vision.md
```

## Start Point
- `docs/start-here.md`
- `docs/control-model.md`
- `docs/routing.md`
