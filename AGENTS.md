## Agent skills

### Issue tracker

Issues and specs are tracked in GitHub Issues. See `docs/agents/issue-tracker.md`.

### Triage labels

Use the canonical triage roles mapped to GitHub labels. See `docs/agents/triage-labels.md`.

### Domain docs

This is a single-context repository using the root `CONTEXT.md` and `docs/adr/`. See `docs/agents/domain.md`.

## RMA Trace

This repository contains a five-person database course project using Spring Boot, MyBatis-Plus, MySQL 8, and a minimal HTML/CSS/JavaScript frontend.

### Read before changing

- For domain terms, scope, and fixed decisions, read `CONTEXT.md`.
- For business behavior, states, pages, APIs, and acceptance scenarios, read `docs/spec/MVP_SPEC.md`.
- For ownership and review boundaries, read `docs/assignments/<member>.md` and `.github/CODEOWNERS`.
- For Fork, branch, commit, and PR steps, read `CONTRIBUTING.md`.

### Repository rules

- Treat GitHub Issues as the source of truth for live task status.
- Keep each pull request scoped to one issue and include test evidence.
- Update the related ER diagram and field documentation in the same pull request when table design changes.
- Use MyBatis-Plus for single-table CRUD and handwritten SQL for joins, reports, and traceability queries.
- Keep Controller, Service, and Mapper responsibilities separate.
- Store only example configuration in Git. Keep credentials in ignored local files.
- Preserve user-authored changes outside the current issue.
- A owns the integrated schema; B, C, D, and E own the first draft of their module tables and ER diagrams.
