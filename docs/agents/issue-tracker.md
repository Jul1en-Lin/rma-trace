# Issue tracker: Gitee

Issues and specs for this repository live in [Gitee Issues](https://gitee.com/Jul1en_lin/rma-trace/issues). The Gitee repository is the only live task source.

## Conventions

- **Create:** use the repository's **新建 Issue** action.
- **Read or list:** use the Gitee Issue identifier, such as `IKD1M5`.
- **Comment:** record design proposals, blockers, review notes, and evidence on the Issue.
- **Labels and status:** edit them on the Gitee Issue page.
- **Close:** close the Issue only after its acceptance conditions and linked PR are complete.

Before changing an Issue, confirm the repository URL is `https://gitee.com/Jul1en_lin/rma-trace`.

## Pull requests as a triage surface

**PRs as a request surface: no.**

Pull requests are submissions linked to existing issues. They are not treated as incoming requests for `/triage`.

Use the full Gitee Issue identifier when referring to a task. Do not reuse the former GitHub issue number.

## When a skill says “publish to the issue tracker”

Create a Gitee Issue.

## When a skill says “fetch the relevant ticket”

Open the matching Gitee Issue and read its description and comments.

## Dependencies

Record dependencies as linked task lists in the Issue body.

A ticket is available only when:

- every blocking issue is closed
- the ticket has no current assignee
- its acceptance conditions are complete enough to act on

For a blocked ticket, add this line near the top of the Issue body:

```text
Blocked by: <linked Gitee Issue identifiers>
```

## Wayfinding

For `/wayfinder`:

- Keep the map in one issue labelled `wayfinder:map`.
- Keep linked tickets in a task list inside the map Issue.
- Label child tickets with `wayfinder:<type>`, such as `research`, `prototype`, `grilling`, or `task`.
- Assign a ticket only when someone or an agent claims it.
- Record the result in the ticket before closing it.
