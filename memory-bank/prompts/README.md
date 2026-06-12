---
title: Prompts Index
doc_kind: prompt
doc_function: index
purpose: Navigation for instantiated reusable prompt documents in the project. Read to find an existing prompt or to create a new one from the governed template.
derived_from:
  - ../dna/governance.md
  - ../flows/templates/prompt/PROMPT-XXX.md
status: active
audience: humans_and_agents
---

# Prompts Index

The `memory-bank/prompts/` directory holds reusable prompt documents for the project.

A prompt document is needed when a prompt has traveled from a rough human formulation to a reusable version that needs to be copied, reviewed, and improved as a memory-bank artifact.

## When to Create a Prompt Document

- The prompt will be reused by a human or an agent.
- The original formulation must be preserved in `source_prompt` while the improved version is kept separately.
- The prompt becomes part of a workflow: review, research, extraction, coding, or agent instructions.

## When a Prompt Document Is Not Needed

- The prompt is one-time only and should not outlive the current dialogue.
- It is a project rule that belongs in `engineering/`, `ops/`, `domain/`, or `AGENTS.md`.
- It is a feature requirement, use case, or ADR rather than an executable instruction for a model.

## Prompt Execution Order

Prompts are listed in SDLC process order. Typically `PROMPT-002` is used at the start when creating `brief.md` and the conditional `design.md`, followed by a human gate; `PROMPT-003` is used when implementation begins.

`PROMPT-001` (issue requirements review) is used to verify that the feature pack meets the requirements stated in a large issue.

`PROMPT-004` (PR review finish) is used when there were post-implementation revisions or when the PR is complex and a thorough review-fix cycle is warranted.

## Registry

| Prompt ID | Title | Status | Prompt status | Kind | Used for | Last updated |
| --- | --- | --- | --- | --- | --- | --- |
| [`PROMPT-001`](PROMPT-001-issue-requirements-review.md) | Issue Requirements Review | `draft` | `drafted` | `review` | Review feature docs against the source issue and memory-bank governance | 2026-05-19 |
| [`PROMPT-002`](PROMPT-002-feature-pack-review-improve.md) | Feature Pack Review Improve | `draft` | `drafted` | `review` | Run bounded review-improve cycles for feature packages | 2026-05-19 |
| [`PROMPT-003`](PROMPT-003-implement-and-test.md) | Implement And Test | `draft` | `drafted` | `coding` | Implement a coding task end-to-end through PR, review/fix and CI | 2026-05-19 |
| [`PROMPT-004`](PROMPT-004-pr-review-finish.md) | PR Review Finish | `draft` | `drafted` | `coding` | Finish an active branch into a ready PR with review-improve and CI gates | 2026-05-19 |

## Naming

- File format: `PROMPT-XXX-short-name.md`
- Replace `XXX` with a stable project identifier: task number, internal prompt id, or a short monotonic number.
- The file title must match the `title` field in frontmatter.

## Template

- Use the template at [`../flows/templates/prompt/PROMPT-XXX.md`](../flows/templates/prompt/PROMPT-XXX.md).
