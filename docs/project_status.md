# Project Status

## Current goal

Goal: Complete the nine-table entity design and prepare module field proposals.

Status: In progress. The reduced MVP, table ownership, relationship skeleton, state rules, and required/optional scope are documented.

Business implementation has not started. The current phase only covers table fields, module ER diagrams, and cross-module relationship review.

## Done

- Initialized and published the repository with the Fork and PR workflow.
- Reduced the first version from sixteen data objects to nine tables.
- Defined the mandatory five-page, single-flow demonstration scope.
- Moved replacement, component batches, dynamic RBAC, deletion, repeated repair, and statistics to optional scope.
- Assigned two or three table drafts to B, C, D, and E; A owns cross-module review and SQL integration.
- Defined the product, application, RMA, inspection, repair, warranty, identifier, and state rules.
- Updated the Spec, project charter, work breakdown, glossary, and individual assignments.

## In progress

- B, C, D, and E review their reduced assignments.
- Module owners propose fields, data types, nullability, indexes, and local constraints.
- A prepares the total ER diagram after reviewing the module proposals.

## Blocked / Questions

- Course requirements for procedures, triggers, views, indexes, tool versions, and report format remain unknown until the teacher briefing.
- `schema.sql` and `demo-data.sql` wait for the four module field proposals and A's relationship review.

## Checkpoints

- 2026-09-27: confirm course requirements and project title.
- 2026-10-13: database design review.
- 2026-10-23: five-minute system presentation.
- 2026-11-01: final report deadline.

## Next actions

1. Let B, C, D, and E review the updated assignment documents.
2. Create one field-design Issue for each member's owned tables.
3. Review the four module ER drafts together before writing the total DDL.
4. Convert the approved fields and relationships into `schema.sql` and `demo-data.sql`.
5. Create implementation Issues only after the database skeleton is approved.
