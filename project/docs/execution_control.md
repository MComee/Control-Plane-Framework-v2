# Execution Control

Execution is single-tool, bounded, and repository-driven.

Control rules:
- execution reads `project/now/`
- execution updates only allowed paths
- execution must not change forbidden paths
- execution writes evidence to `project/evidence/`

Handoff contract:
1. `project/now/description.md` states the active objective.
2. `project/now/prompt.md` states exact execution requirements.
3. `project/now/metadata.json` enforces allowed and forbidden paths.

Validation contract:
- confirm required checks in metadata
- confirm boundary compliance
- confirm repository structure integrity
