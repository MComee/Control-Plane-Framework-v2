# Control Model

This document outlines the layered control model of the Control Plane Framework v2, detailing how governance and execution are managed within the repository.

## Control Layers:

The framework employs a three-layer control model to ensure integrity, project alignment, and guided execution.

### Layer 1 — Framework Self-Governance:

This foundational layer protects the framework's core doctrines and operational integrity. It governs:
*   **Framework Doctrine:** Adherence to the principles and vision of the Control Plane Framework.
*   **Routing Rules:** The mechanisms and logic that dictate information flow and task execution.
*   **Protected Paths:** Files and directories that are considered sensitive or critical and are subject to strict access control.
*   **Planning Synchronization:** Ensuring that all planning artifacts within the repository are consistent and up-to-date.
*   **Execution Boundaries:** Defining and enforcing the limits within which external tools or operators can perform actions.

### Layer 2 — Single-Project Control:

This layer focuses on governing the specific project being managed by the repository. It operates under the `project/` directory and protects and governs:
*   **`project/vision/`:** The core vision, constraints, and brainstorming for the project.
*   **`project/docs/`:** All project-specific documentation, including features, task groups, tasks, priorities, roadmap, decisions, definition of done, and execution control.
*   **`project/now/`:** The active work state, including descriptions, prompts, and metadata for current tasks.
*   **`project/evidence/`:** Storage for artifacts, run logs, and test runs generated during execution.

### Layer 3 — Execution Guidance:

This layer guides external tools (e.g., AI assistants) by providing explicit instructions on how to interact with the repository and execute tasks. It achieves this by:
*   **Read Instructions:** Clearly specifying which files or parts of the repository an AI tool may read.
*   **Modification Permissions:** Explicitly stating which files an AI tool is permitted to change.
*   **Prohibited Actions:** Defining files or operations that must not be modified or accessed.
*   **Handoff Source:** Utilizing `project/now/prompt.md` as the definitive source for the current task's objectives, scope, and requirements.

This layered model ensures that the framework maintains control over its own integrity, the project it manages, and the execution of tasks against the repository's truth.
