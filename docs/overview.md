# Overview

Control Plane Framework v2 is a repository-native control system for AI-assisted software development.

It governs:
- repository truth
- planning synchronization to files
- one-project control state
- execution handoff through `project/now/`
- boundary-aware validation

It does not govern:
- model internals
- hidden tool behavior
- vendor-specific orchestration internals

One repository instance controls one project. Planning is valid only when synchronized to repository files.

Root `README.md` is the universal entrypoint and must remain an exact mirror of tracked repository paths.
