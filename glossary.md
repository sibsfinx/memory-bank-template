---
title: Glossary
purpose: Definitions of key terms used across the memory-bank template.
status: active
derived_from:
  - memory-bank/dna/governance.md
---

# Glossary

**Durable Knowledge Layer** — A resilient knowledge layer for projects: versioned documents preserving important context across sessions, participants, and code changes. In this repository, `memory-bank` serves as this structured documentation layer with governance rules, SSoT, and explicit document connections.

**SSoT** (Single Source of Truth) — A principle where each fact has exactly one canonical owner. Duplication across multiple locations constitutes a documentation defect.

**Canonical Owner** — A document owning a specific fact with priority over downstream descriptions. Changes to such documents represent source-of-truth modifications.

**Governed Document** — A markdown file following repository governance rules, typically with valid YAML frontmatter, clear role definition, and explicit upstream connections.

**Authoritative Document** — A governed document currently serving as the active source of truth, marked with `status: active`.

**Dependency Tree** — Document interconnections via `derived_from`, where authority flows upstream to downstream, requiring updates to derived materials when source documents change.

**Upstream and Downstream** — Upstream documents are sources providing context; downstream documents inherit that context without contradiction.

**Derived From** — A frontmatter field listing direct upstream documents, making knowledge origins explicit.

**Progressive Disclosure** — Documentation organization providing brief overviews first, with detailed information accessible through links.

**Index-First** — Rule requiring all significant documents be discoverable from an index; unreferenced orphan files constitute defects.

**Documentation Layer** — Structured knowledge with document roles, navigation, and responsibility boundaries, residing in `memory-bank/`.

**Process Layer** — Knowledge describing lifecycles, workflows, gates, and execution templates, mainly in `memory-bank/flows/`.

**Instantiated Document** — Project-specific documents created from templates with real context.

**Wrapper Template** — A governed template document containing an embedded contract for future instantiated documents.

**Embedded Template Contract** — The portion copied into new instantiated documents, containing frontmatter and body.

**Feature Package** — Directory `FT-XXX/` containing delivery-unit documents: canonical `brief.md`, optional `design.md`, execution plans, related ADRs, and local index.

**PRD** (Product Requirements Document) — Initiative-level document capturing what and why changes occur before feature decomposition.

**ADR** (Architecture Decision Record) — Document recording architectural decisions, context, and rationale, primarily addressing "why" decisions.

**Status** — Publication status (`draft`, `active`, `archived`) indicating whether documents represent current truth.

**Delivery Status** — Feature lifecycle status (`planned`, `in_progress`, `done`, `cancelled`), separate from publication status.

**Decision Status** — ADR lifecycle status (`proposed`, `accepted`, `superseded`, `rejected`) reflecting decision outcomes.
