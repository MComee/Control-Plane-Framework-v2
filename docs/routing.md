# Routing

This document describes the routing and information flow within the Control Plane Framework v2, ensuring that work is directed effectively and predictably.

## Core Routing Principles:

*   **Centralized Control:** All execution guidance originates from the `project/now/` directory. This is the primary handoff point for AI tools and developers.
*   **Repository as Single Source of Truth:** Information consumed for planning and execution must be sourced from the repository files. This ensures consistency and avoids external state drift.
*   **Framework-Managed Navigation:** The framework dictates which files can be read and modified by external tools. This is managed via `project/now/metadata.json` (`allowed_paths`, `forbidden_paths`) and framework rules.
*   **Clear Handoffs:** Execution tasks are defined in `project/now/prompt.md`. These prompts specify the objective, required reads, allowed modifications, and validation criteria.
*   **Validation at Boundaries:** All changes made by external tools are subject to validation against framework rules and protected boundaries to ensure integrity.

## Execution Flow:

1.  **Task Definition:** A task is defined and prioritized, leading to its activation in `project/now/`.
2.  **Contextualization:** `project/now/metadata.json` and `project/now/prompt.md` are populated with task details, including allowed and forbidden paths.
3.  **AI/Developer Handoff:** An AI tool or developer receives the prompt from `project/now/prompt.md`.
4.  **Information Consumption:** The tool/developer reads information from specified repository locations (as defined in `project/now/metadata.json` and the prompt).
5.  **Execution & Modification:** The tool/developer performs actions, making modifications only to files explicitly permitted by `project/now/metadata.json` and the prompt.
6.  **Validation:** Framework mechanisms verify that all actions adhered to the `allowed_paths`, `forbidden_paths`, and other defined constraints.
7.  **Evidence & State Update:** Results and evidence are stored in `project/evidence/`, and the active work state is updated.

This structured routing ensures that development is controlled, traceable, and aligned with the framework's principles.
