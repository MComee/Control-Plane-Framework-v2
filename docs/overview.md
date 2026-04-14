# Overview

The Control Plane Framework v2 is designed to facilitate AI-assisted software development by establishing and maintaining a clear, disciplined structure within a Git repository. It acts as a control mechanism, ensuring that development processes are predictable, traceable, and aligned with the project's vision.

## Key Concepts:

*   **Repository as Truth:** The framework treats the Git repository as the ultimate source of truth for all project artifacts, plans, and execution states. It does not manage AI model internals but guides their application within the repository context.
*   **Single Project Governance:** Each repository instance is dedicated to governing a single project, preventing scope creep and maintaining focus.
*   **Synchronized Planning:** Project plans are not external documents but integrated components of the repository. Changes to plans must be committed to the repository, ensuring all stakeholders (human and AI) work from the same information.
*   **Active Work Context:** The `project/now/` directory serves as the dynamic workspace for current tasks. AI tools and developers consume instructions from `project/now/prompt.md` and operate within the defined `project/now/metadata.json` constraints.
*   **Execution Boundary Enforcement:** The framework includes mechanisms to define and validate protected areas and operations within the repository, ensuring that AI tools and developers respect established boundaries and do not introduce unintended changes.

## Architecture:

The framework enforces a specific repository structure to maintain clarity and discipline. Key components include:

*   `project/`: Contains all project-specific artifacts, including vision, documentation, priorities, active work, and evidence.
*   `framework/`: Houses the core framework logic, rules, and templates.
*   `docs/`: Centralized documentation for the framework and the controlled project.
*   `project/now/`: The operational heart for current tasks, containing descriptions, prompts, and metadata.

Refer to the root `README.md` for a comprehensive and recursive file tree of the repository.
