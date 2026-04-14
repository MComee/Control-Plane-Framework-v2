# Routing

Routing controls how one external tool receives and executes active work.

## Routing Rules
- Repository files are the only authoritative execution source.
- Handoff source is `project/now/prompt.md`.
- Boundary source is `project/now/metadata.json` (`allowed_paths`, `forbidden_paths`).
- Execution updates only approved paths and writes evidence to `project/evidence/`.
- Validation must confirm boundary compliance and path integrity.
- Root `README.md` tree must be updated whenever tracked paths change.

## Flow
1. Planning state is synchronized under `project/docs/` and `project/now/`.
2. One active task is exposed in `project/now/`.
3. One tool executes against required reads and allowed paths.
4. Tool records evidence under `project/evidence/`.
5. Validation verifies boundaries and repository-structure compliance.
