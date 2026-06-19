---
title: Development Environment
doc_kind: ops
doc_function: canonical
purpose: Template for local development setup. Read when adapting initialization routines and daily workflows to the project.
derived_from:
  - ../dna/governance.md
status: active
audience: humans_and_agents
---

# Development Environment

## Setup

Document canonical commands for environment preparation. Remove examples that do not apply.

```bash
make setup
npm install / pnpm install
docker compose up -d
direnv allow
asdf install
uv sync
bundle install
```

## Daily Commands

Document canonical local commands that agents and developers should use.

```bash
make dev          # start dev server
docker compose up # start services
pnpm dev          # frontend dev server
pytest            # run Python tests
bundle exec rspec # run Ruby tests
go test ./...     # run Go tests
```

## Browser Testing

For projects with a UI, document:

- How to determine the local URL (check `DEV_HOST` or `.env` first, fall back to documented defaults)
- Port and host configuration source
- Whether automated discovery is possible
- The canonical verification approach

Example workflow: check `DEV_HOST` or `.env` first, fall back to documented defaults, do not manually scan ports without an explicit user request.

## Database And Services

Document only operationally critical elements:

- Database migration command
- Local database recreation command
- Required services and how to start them
- Seeded datasets available locally
- Known local development pitfalls

## Adoption Checklist

- [ ] Real setup commands specified (not example placeholders)
- [ ] Actual test/lint commands included
- [ ] Local URL determination documented
- [ ] Dependencies listed
- [ ] Irrelevant examples removed
