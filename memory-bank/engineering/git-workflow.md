---
title: Git Workflow
doc_kind: engineering
doc_function: canonical
purpose: Git conventions for the project: commits, branches, PRs, and optional worktrees.
derived_from:
  - ../dna/governance.md
status: active
audience: humans_and_agents
---

# Git Workflow

## Default Branch

`main` (or specify: `master`, etc.)

## Commits

- Present-tense, concise: `fix: normalize cache key`, `feat: add user export endpoint`
- Optional: reference the issue or ticket in the footer
- Auto-close keywords: `Closes #123` (if used)
- Squash merge expectation: yes / no

## Pull Requests

- All local checks must pass before submission
- PR title: concise and descriptive
- PR body should document: what changed, how it was tested, and any remaining risks
- Required reviewers: (specify)

## Worktrees

(Remove this section if not applicable to the project.)

- Create worktrees in: `../worktrees/<branch-name>/`
- Run bootstrap script after creation: `make setup` / `bin/setup` / etc.
- Prohibited directories for temporary work: `tmp/`, `log/`

## Branch Naming

| Type | Pattern | Example |
| --- | --- | --- |
| Feature | `feat/<issue-id>-short-name` | `feat/123-user-export` |
| Fix | `fix/<issue-id>-short-name` | `fix/456-cache-key` |
| Chore | `chore/<description>` | `chore/update-deps` |
