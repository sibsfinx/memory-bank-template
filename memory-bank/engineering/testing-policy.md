---
title: Testing Policy
doc_kind: engineering
doc_function: canonical
purpose: Testing rules, required automated tests, and sufficient coverage definition. Answers the question — when must a feature have test cases and when is manual-only verify acceptable.
derived_from:
  - ../dna/governance.md
  - ../flows/feature-flow.md
status: active
audience: humans_and_agents
---

# Testing Policy

## Core Principle

Any deterministically-verifiable behavioral change must have automated regression coverage. Contract-level changes and bug fixes require automated verification and regression tests.

Manual-only testing is permitted only as an explicit exception where automation is not realistic.

## Lifecycle Gates

Testing requirements are aligned with the feature flow lifecycle:

| Gate | Testing requirement |
| --- | --- |
| Problem Ready | Test inventory in `brief.md`: at least one `SC-*`, traceability to `REQ-*`, Design Requirement Decision |
| Solution Ready | `design.md` captures contracts and failure modes; C4 applicability decided |
| Plan Ready | `implementation-plan.md` documents test strategy: automated coverage surfaces, required local/CI suites |
| Done | Required tests passing locally and in CI; all `CHK-*` and `EVID-*` filled in `brief.md` |

## Sufficient Coverage Definition

Sufficient coverage includes:

- Scenario and contract-level verification of the changed behavior
- Critical failure modes
- Feature-specific edge cases and negative scenarios

Line coverage percentage alone is not sufficient.

## Manual-Only Exceptions

Manual-only testing is allowed only when automation is genuinely not realistic (live infrastructure, hardware, non-deterministic environment). Each manual-only gap requires:

- A reason why automation is not possible
- A manual procedure or `EVID-*`
- An owner follow-up
- An approval reference via `AG-*`

## Simplify Review

A separate pass after functional tests and before closure. Goal: ensure the code is minimally complex. Complexity is justified only by reference to `CON-*`, `INV-*`, `FM-*`, `SD-*`, or an accepted ADR.

## Verification Context Separation

Functional verification, simplify review, and acceptance testing are three logically separate passes. The agent formulates conclusions from each pass before beginning the next. For small features all three may occur in one session, but the simplify review must not be skipped.

## Project Adaptation

Specify for this project:

- Test frameworks: (e.g. RSpec, pytest, Jest, go test)
- Data strategy: (factories, fixtures, seeds)
- Local test command: `bundle exec rspec` / `pytest` / `npm test`
- CI job: (job name and config file)
