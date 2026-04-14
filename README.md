# Control Plane Framework v2

## Purpose
This repository is a framework for controlling AI-assisted project development in a single project context. It defines governance, planning synchronization, execution boundaries, and validation expectations.

The framework is not an application. It does not prescribe product logic or implementation technology.

## Control Layers
### 1. Self-governing framework layer
- Protects framework and planning doctrine from uncontrolled edits.
- Prevents drift of control logic.
- Defines routing and behavior rules for planning, execution, and validation.

### 2. Single-project control layer
- Enforces one project per repository under `project/`.
- Governs vision, features, task groups, tasks, priorities, active work, and evidence.

### 3. Tool-agnostic execution guidance layer
- Does not control AI tools directly.
- Guides tools with structured context and prompts.
- Aligns execution across ChatGPT, Gemini, Claude, Codex CLI, and local tools.

## Workflow
1. Planning
2. Prioritization
3. Handoff
4. Execution
5. Validation

Planning artifacts are persisted in `project/docs/` and `project/vision/`. Execution is routed through `project/now/`. Validation is recorded under `project/evidence/`.

## Repository Tree
```text
README.md

docs/
  overview.md
  start-here.md
  routing.md
  control-model.md

framework/
  rules/
    protected-files.md
    planning-sync.md
    execution-boundaries.md
  templates/
    feature-template.md
    task-group-template.md
    task-template.md
    active-work-template.md

project/
  vision/
    core_vision.md
    constraints.md
    brainstorming.md

  docs/
    features/
      README.md
    task_groups/
      README.md
    tasks/
      README.md
    priorities/
      now.md
      next.md
      later.md
      blocked.md
      done.md
      roadmap.md
      decisions.md
      definition_of_done.md

  now/
    description.md
    prompt.md
    metadata.json

  evidence/
    run_logs/
    test_runs/
    artifacts/

  app/
    README.md
```

## How AI tools should use this repo
1. Read `README.md` first.
2. Determine current phase: planning, prioritization, handoff, execution, or validation.
3. Follow routing rules in `docs/routing.md`.
4. Never mutate protected files unless explicitly allowed by framework rules.
5. Use `project/now/prompt.md` as the execution prompt source during execution.
