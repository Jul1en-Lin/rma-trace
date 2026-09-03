# Domain Docs

This is a single-context repository.

## Before exploring

Read:

- `CONTEXT.md` at the repository root
- relevant ADRs under `docs/adr/`

If an ADR directory or relevant ADR does not exist, proceed silently. Create ADRs only when a real decision needs to be recorded.

## Layout

```text
/
├── CONTEXT.md
├── docs/
│   ├── adr/
│   └── agents/
└── src/
```

## Use the glossary vocabulary

Use the domain terms defined in `CONTEXT.md` in issue titles, specifications, code names, tests, and explanations.

Do not replace a defined term with a synonym that the glossary explicitly avoids.

If a required concept is missing, either reconsider the new term or record the gap for `/domain-modeling`.

## ADR conflicts

If proposed work conflicts with an existing ADR, identify the conflict explicitly instead of silently replacing the earlier decision.
