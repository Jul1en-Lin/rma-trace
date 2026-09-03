# Issue tracker: GitHub

Issues and specs for this repository live as GitHub issues. Use the `gh` CLI for tracker operations.

## Conventions

- **Create an issue:** `gh issue create --title "..." --body "..."`
- **Read an issue:** `gh issue view <number> --comments`
- **List issues:** `gh issue list --state open`
- **Comment:** `gh issue comment <number> --body "..."`
- **Apply or remove labels:** use `gh issue edit`
- **Close:** `gh issue close <number> --comment "..."`

Infer the repository from `git remote -v`. When running inside this clone, `gh` normally resolves `Jul1en-Lin/rma-trace` automatically.

## Pull requests as a triage surface

**PRs as a request surface: no.**

Pull requests are implementation submissions linked to existing issues. They are not treated as incoming feature requests for `/triage`.

GitHub shares one number space across issues and pull requests. When a bare number is ambiguous, try `gh pr view <number>` and then `gh issue view <number>`.

## When a skill says “publish to the issue tracker”

Create a GitHub issue.

## When a skill says “fetch the relevant ticket”

Run `gh issue view <number> --comments`.

## Dependencies

Use GitHub native issue dependencies when available.

A ticket is available only when:

- every blocking issue is closed
- the ticket has no current assignee
- its acceptance conditions are complete enough to act on

If native dependencies are unavailable, add this line near the top of the issue body:

```text
Blocked by: #<number>, #<number>
```

## Wayfinding

For `/wayfinder`:

- Keep the map in one issue labelled `wayfinder:map`.
- Link decision tickets as sub-issues when GitHub supports them.
- Otherwise, keep the tickets in a task list inside the map issue.
- Label child tickets with `wayfinder:<type>`, such as `research`, `prototype`, `grilling`, or `task`.
- Assign a ticket only when someone or an agent claims it.
- Record the result in the ticket before closing it.
