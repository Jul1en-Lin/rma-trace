<!-- BEGIN: setup-long-term-docs -->

## Lightweight agent workflow

This repository uses a small project memory setup for short-lived projects, scripts, demos, and experiments.

### Documentation sources of truth

- `docs/project_status.md`: current goal, progress, blockers, checks, and next actions.
- `docs/agent_workflow.md`: lightweight status, commit, and handoff workflow.

### Required rules

- Read `docs/project_status.md` before making changes when it exists.
- Update `docs/project_status.md` when meaningful progress is made, a blocker appears or is resolved, the next action changes, or work should be resumable later.
- Keep updates short. Do not create extra planning documents unless the user asks.
- Before any git commit, check whether `docs/project_status.md` should be updated.
- Commit only files related to the current work. Do not sweep unrelated files into commits.
- Do not push unless the user explicitly asks or the current task grants push/publish authorization.
- Summarize changed files, checks run, and remaining risks.

### Detailed workflows

For status, commit, and handoff details, read `docs/agent_workflow.md`.

<!-- END: setup-long-term-docs -->
## RMA Trace

This repository contains a five-person database course project using Spring Boot, MyBatis-Plus, MySQL 8, and a minimal HTML/CSS/JavaScript frontend.

### Read before changing

- For domain terms, scope, and fixed decisions, read `CONTEXT.md`.
- For business behavior, states, pages, APIs, and acceptance scenarios, read `docs/spec/MVP_SPEC.md`.
- For ownership and review boundaries, read `docs/assignments/<member>.md` and `CODEOWNERS`.
- For Fork, branch, commit, and PR steps, read `CONTRIBUTING.md`.

### Repository rules

- Treat GitHub Issues as the source of truth for live task status.
- Keep each pull request scoped to one issue and include test evidence.
- Update the related ER diagram and field documentation in the same pull request when table design changes.
- Use MyBatis-Plus for single-table CRUD and handwritten SQL for joins, reports, and traceability queries.
- Keep Controller, Service, and Mapper responsibilities separate.
- Store only example configuration in Git. Keep credentials in ignored local files.
- Preserve user-authored changes outside the current issue.
- A owns the integrated schema; C, D, and E own the first draft of their module tables and ER diagrams.
