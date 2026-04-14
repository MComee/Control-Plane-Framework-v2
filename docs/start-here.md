# Start Here

This document guides you through setting up and using the Control Plane Framework v2.

## Core Principles:

*   **Repository Truth, Not AI Internals:** This framework governs the state and truth of the repository, not the internal workings of AI models. It provides structure and guidance for AI-assisted development processes.
*   **Single Project Control:** Each instance of this repository controls exactly one project. This ensures clarity and prevents conflicts when managing different projects.
*   **Repository-Centric Planning:** All planning activities must be synchronized with and reflected in the repository's files. This ensures a single source of truth for project direction.
*   **Execution Driven by Active Work:** AI tools and human operators must consume and act upon the current state defined in `project/now/`. This ensures that work is always based on the latest, approved active tasks.
*   **Protected Boundary Validation:** All operations must be validated to ensure that protected boundaries (defined in framework rules and configuration) were respected. This maintains framework integrity and prevents unintended side effects.

## Getting Started:

1.  **Understand the Vision:** Review `project/vision/core_vision.md` to grasp the project's overall goals.
2.  **Explore Documentation:** Familiarize yourself with `docs/overview.md`, `docs/routing.md`, and `docs/control-model.md`.
3.  **Initiate Active Work:** Define the current task in `project/now/` and update `project/now/metadata.json`.
4.  **Follow Execution Guidance:** Use the instructions in `project/now/prompt.md` to guide your actions.
5.  **Validate Changes:** Ensure all changes adhere to the framework's principles and protected boundaries.

## Framework Structure:

Refer to the root `README.md` for a complete, recursive file tree of the repository.
