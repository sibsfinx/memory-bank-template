# Repository Rules

## Project Structure

The `memory-bank/` directory contains a generic, reusable template. Project-specific adaptations belong in the downstream layers (product, domain, engineering, ops). Generic rules stay in the template; specialized implementations do not flow back into it.

## Development Workflow

This repository uses lightweight checks instead of an automated test suite:

```bash
# Check file structure
rg --files memory-bank/

# Audit links and navigation
python3 scripts/check_memory_bank_index.py

# Check whitespace
git diff --check

# Ensure no project-specific terminology leaked into the template
rg "your-project-name" memory-bank/
```

## Documentation Standards

- **Format**: Markdown with relative links
- **Frontmatter**: Governed documents require valid YAML frontmatter with a mandatory `status` field. Non-root active documents must include `derived_from`.
- **Naming**: Lowercase kebab-case (e.g., `testing-policy.md`). Structured artifacts follow template patterns such as `ADR-XXX-*.md`.
- **Links**: Use relative paths; annotate links to clarify what the reader will find.

## Review Guidelines

Manual code review checks for:
- Index and link consistency with the new structure
- Absence of project-specific details inside `memory-bank/`
- Alignment between modified template documents and their neighboring files
- No contradictions between documents that share `derived_from` relationships

## Git Conventions

Commit messages use present-tense conventions:

```
docs: tighten template ops guidance
docs: add epic flow lifecycle diagram
fix: repair broken link in domain README
```

Pull requests should describe template changes and list affected references or naming rules.
