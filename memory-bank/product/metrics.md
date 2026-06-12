---
title: Product Metrics
doc_kind: product
doc_function: canonical
purpose: Canonical place for product success metrics, baselines, targets, measurement ownership, and instrumentation constraints.
derived_from:
  - ../dna/governance.md
  - context.md
status: active
audience: humans_and_agents
canonical_for:
  - product_metrics
  - measurement_contracts
---

# Product Metrics

This document captures product metrics and measurement rules. Feature-level evidence stays within feature packages. This document owns product-level outcomes and measurement contracts.

## North Star Metric

| Metric | Why it matters | Baseline | Target | Review cadence |
| --- | --- | --- | --- | --- |
| Name the primary success indicator | Why this metric captures product health | Current value | Desired value | How often we review |

## Product Metrics

| Metric ID | Metric | Owner | Baseline | Target | Measurement method | Data source |
| --- | --- | --- | --- | --- | --- | --- |
| `MET-01` | What we measure | Who owns this metric | Current value | Desired value | How we measure | Canonical data source |

## Guardrails

Thresholds that must not regress. If a guardrail is breached, stop and investigate before continuing delivery.

| Guardrail ID | Metric | Threshold | Response protocol |
| --- | --- | --- | --- |
| `GRD-01` | What must not worsen | Minimum acceptable value | What to do when breached |

## Instrumentation Constraints

- Which data sources are authoritative for each metric.
- Factors affecting metric interpretation: data latency, sampling rates, privacy rules.

## Metric Change Policy

- If a metric definition is modified within a feature package, this document must be updated or the upstream PRD must be updated first.
- Newly introduced local metrics remain within feature packages until they become shared product metrics.
