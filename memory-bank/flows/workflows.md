---
title: Task Workflows
doc_kind: governance
doc_function: canonical
purpose: Task routing by type and base development cycle. Read when receiving a new task to choose the right approach.
derived_from:
  - ../dna/governance.md
  - feature-flow.md
canonical_for:
  - task_routing_rules
  - base_development_cycle
  - workflow_type_selection
  - autonomy_gradient
status: active
audience: humans_and_agents
---

# Task Workflows

## Base Cycle

Every workflow is a chain of repetitions of one cycle:

```text
Artifact → Review → Polish
                  → Decompose
                  → Accepted
```

An artifact is what is created at each stage: brief, design doc, plan, code, PR, runbook.

## Human Participation Gradient

The closer to business requirements, the more human involvement. The closer to code and local verification, the more the agent works autonomously.

```text
Business requirements  ← human  |  agent →  Code
  PRD, Use Cases         Brief, Design, Plan   PR, Tests
```

## Workflow Types

### 1. Small Feature

When:

- The task is clear
- The scope is local
- The solution fits in one session or one compact change set

Flow:

`issue/task -> routing -> implementation -> review -> merge`

### 2. Medium Or Large Feature

When:

- Touches multiple layers
- Requires design choices
- Needs checkpoints and an explicit execution plan

Flow:

`issue/task -> feature package -> brief -> optional design -> implementation plan -> execution -> review -> handoff`

### 3. Bug Fix

Sources can be anything: error tracker, support, QA, direct user report, incident analysis.

Flow:

`report -> reproduction -> analysis -> fix -> regression coverage -> review`

### 4. Refactoring

Split into at minimum three classes:

- In-line during a delivery task
- Exploratory
- Systemic, with a large change surface

Exploratory and systemic refactoring usually require an explicit plan and checkpoints.

### 5. Incident / PIR

Flow:

`incident -> timeline -> root cause analysis -> fixes -> prevention work`

A human typically confirms the RCA and follow-up task priorities.

## Routing Rules

Use the minimum workflow that does not lose control over risk.

- If the task is small and clear, do not inflate it into a large feature package.
- If the task changes a contract, rollout, or requires approvals, escalate it to the feature flow.
- If review comments do not diminish after iterations, the problem may be upstream rather than in the code.
