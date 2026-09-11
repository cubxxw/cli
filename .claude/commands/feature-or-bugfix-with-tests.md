---
name: feature-or-bugfix-with-tests
description: Workflow command scaffold for feature-or-bugfix-with-tests in cli.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /feature-or-bugfix-with-tests

Use this workflow when working on **feature-or-bugfix-with-tests** in `cli`.

## Goal

Implements a new feature or fixes a bug, accompanied by corresponding test updates.

## Common Files

- `internal/skills/registry/registry.go`
- `internal/skills/registry/registry_test.go`
- `pkg/cmd/skills/install/install.go`
- `pkg/cmd/skills/install/install_test.go`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit or create implementation file(s) in the relevant internal or pkg directory.
- Edit or create corresponding test file(s) in the same directory.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.