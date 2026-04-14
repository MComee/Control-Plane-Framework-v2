# Control Model

## Layer 1: Framework self-governance
The framework layer defines immutable control doctrine, routing behavior, and mutation boundaries. It exists to protect structure and prevent control drift.

Responsibilities:
- Define protected and restricted paths.
- Define planning synchronization requirements.
- Define execution boundaries and evidence expectations.

## Layer 2: Project control
The project layer contains project-specific planning and control state under `project/`.

Responsibilities:
- Vision and constraints.
- Feature and task decomposition.
- Prioritization and active work state.
- Evidence records linked to execution.

## Layer 3: Execution guidance
The execution guidance layer provides structured, tool-agnostic handoff for implementation work.

Responsibilities:
- Define current step and objective.
- Provide machine-readable and machine-actionable prompts.
- Keep execution aligned with project control without direct tool lock-in.

## Separation of concerns
- Layer 1 governs process integrity.
- Layer 2 governs project intent and planning state.
- Layer 3 governs immediate execution behavior.

Each layer has a distinct scope. Execution must not rewrite governance doctrine. Planning must not exist only in conversation. Validation must confirm both output quality and boundary compliance.
