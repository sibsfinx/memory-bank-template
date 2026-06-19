---
title: Domain Glossary
doc_kind: domain
doc_function: canonical
purpose: Canonical place for ubiquitous language, domain terms, prohibited ambiguities, and naming decisions.
derived_from:
  - ../dna/governance.md
status: active
audience: humans_and_agents
canonical_for:
  - ubiquitous_language
  - domain_terms
---

# Domain Glossary

This document records the language of the subject domain. If a term is defined here, downstream documents use this meaning or explicitly explain any exception.

## Terms

| Term | Meaning | Context | Do not confuse with |
| --- | --- | --- | --- |
| `domain-term` | What the term means in this project | Where it is used | Similar product, UI, or technical terms |

## Naming Rules

- Use domain terms consistently in PRDs, use cases, features, code comments, and ADRs.
- Do not introduce a new synonym for an existing domain concept without updating this glossary.
- UI labels may differ from domain terms, but the difference must be explained in product or UX documents.

## Ambiguous Terms

| Term | Allowed meaning | Forbidden / overloaded meaning | Replacement |
| --- | --- | --- | --- |
| `ambiguous-term` | What is allowed | What causes confusion | Which term to use instead |

## Source Documents

- Add links to domain research, legal/compliance definitions, legacy docs, or SME notes.
- If no sources exist yet, write `unknown` and do not invent an origin for the term.
