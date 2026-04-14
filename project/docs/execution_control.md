# Execution Control

Execution is single-tool, bounded, and repository-driven.

Control rules:
- execution consumes `project/now/`
- execution handoff source is `project/now/prompt.md`
- execution updates only allowed paths
- execution must not change forbidden paths
- execution writes evidence to `project/evidence/`
- if tracked paths change, root `README.md` tree must be updated in the same change set

Validation contract:
- confirm required checks in metadata
- confirm boundary compliance
- confirm structure integrity
- confirm README tracked-path tree accuracy
