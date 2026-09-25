---
name: multi-docs-update
description: Workflow command scaffold for multi-docs-update in cli.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /multi-docs-update

Use this workflow when working on **multi-docs-update** in `cli`.

## Goal

Updates multiple documentation files, often to fix errors, improve clarity, or correct links.

## Common Files

- `docs/install_linux.md`
- `docs/install_macos.md`
- `docs/install_windows.md`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit multiple documentation files (e.g., README, install guides) to fix errors or improve content.
- Commit all related documentation changes together.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.