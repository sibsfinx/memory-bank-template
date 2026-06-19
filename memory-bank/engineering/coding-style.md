---
title: Coding Style
doc_kind: engineering
doc_function: canonical
purpose: Code formatting conventions, tooling, and local complexity rules for the project.
derived_from:
  - ../dna/governance.md
status: active
audience: humans_and_agents
---

# Coding Style

## General Rules

- File, module, and directory names must follow the conventions of the project's primary language.
- Add comments only where the logic or boundary conditions are unclear. Do not explain what the code does; name identifiers clearly instead.
- Favor simple local solutions over premature abstractions. Three similar lines are better than a premature abstraction.
- Generated, vendored code, and migrations follow separate guidelines as defined.

## Tooling Contract

Document the canonical tools for this project:

| Tool role | Tool | Config file | Run command |
| --- | --- | --- | --- |
| Formatter | e.g. prettier, ruff, rubocop, gofmt | `.prettierrc` / `pyproject.toml` / ... | `npm run format` / ... |
| Linter | e.g. eslint, ruff, rubocop, golangci-lint | `.eslintrc` / ... | `npm run lint` / ... |
| Pre-commit | optional | `.pre-commit-config.yaml` | `pre-commit run` |

## Language-Specific Addendum

Add real conventions for the project tech stack here:

**Backend:**

- Naming conventions (functions, classes, modules)
- Error handling patterns
- Module organization rules
- Typing discipline

**Frontend:**

- Component conventions
- State management approach
- Styling rules

**Database:**

- Migration naming and sequencing
- Index conventions

## Change Discipline

- Do not rewrite unrelated code purely for consistency during a focused change.
- Follow the local file style during minor updates unless it conflicts with canonical rules.
- When transitioning between frameworks or style approaches, document migration rules explicitly.
