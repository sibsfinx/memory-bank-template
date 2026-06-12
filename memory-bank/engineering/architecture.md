---
title: Engineering Architecture Patterns
doc_kind: engineering
doc_function: canonical
purpose: Canonical place for implementation architecture rules: code/module boundaries, runtime patterns, concurrency, error handling, and configuration ownership.
derived_from:
  - ../dna/governance.md
  - ../domain/context-map.md
status: active
audience: humans_and_agents
---

# Engineering Architecture Patterns

This document establishes expected implementation architecture rules. Domain bounded contexts are described in [`../domain/context-map.md`](../domain/context-map.md); record here how they are reflected in code modules, services, queues, adapters, and configuration ownership.

## Module Boundaries

Record the main isolated implementation areas.

Example:

| Module / Layer | Owns | Must not depend on directly |
| --- | --- | --- |
| `customer-facing` | user path, public APIs | internal admin details |
| `operations` | backoffice, manual actions, moderation | private internals of billing/storage |
| `platform` | shared services, auth, delivery infrastructure | product-specific UI assumptions |

Minimum rules:

- a module owns its state and public contracts;
- cross-module dependencies go through an explicitly named API, event, or adapter;
- UI, jobs, and integrations must not read another module's internal details bypassing the owner module.

## Concurrency And Critical Sections

If the project contains concurrent operations, record the canonical pattern for critical sections and background work.

Example:

```ruby
ResourceLock.with_lock(resource_key) do
  # critical section
end
```

Specify explicitly:

- which locking pattern is allowed;
- which pattern is forbidden and why;
- what counts as idempotent recovery;
- where transaction boundaries lie relative to external APIs.

If the project uses a job queue, add a canonical rule for concurrency control.

## Failure Handling And Error Tracking

Record a single approach:

- where errors are propagated up vs. converted into a domain verdict;
- how contextual metadata is added to the error tracker;
- where retry policy is already implemented by infrastructure and must not be duplicated by a local `rescue`.

Example question this section should answer:

> Do I need to manually log an error in a job if the base job class already handles retries and notifications?

## Configuration Ownership

Document not every environment variable in sequence, but the ownership model of configuration:

- where the canonical configuration schema lives;
- which files or classes are considered the owner layer;
- where defaults are set;
- who is responsible for documenting the env contract.

Example:

1. Update the configuration schema owner.
2. Update default values or environment overlays.
3. Update [`../ops/config.md`](../ops/config.md).
