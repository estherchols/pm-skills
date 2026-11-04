---
name: user-stories
description: Break a feature, PRD, or epic into user stories with acceptance criteria ready for a backlog (Jira, Linear, GitHub Issues). Use when the user asks for user stories, tickets, backlog items, acceptance criteria, Gherkin scenarios, story splitting, or "break this down for engineering".
---

# User Stories

Convert a feature description or PRD into well-formed, independently shippable user stories.

## Process

1. **Identify the epic** and the personas involved.
2. **Map the user journey** — list the steps a user takes end to end. Each step is a candidate story.
3. **Write stories** in the standard format:
   > **As a** [specific persona], **I want** [capability], **so that** [outcome/value].
4. **Add acceptance criteria** for each story (see below).
5. **Split anything too big** (see splitting patterns).
6. **Order** stories so the first slice delivers a thin, end-to-end usable path (walking skeleton) before enhancements.

## Acceptance criteria

Default to Given/When/Then (Gherkin). Cover the happy path, at least one edge case, and one error case:

```gherkin
Scenario: Successful export
  Given I am an admin viewing the Reports page
  When I click "Export CSV"
  Then a CSV with all visible columns downloads within 5 seconds

Scenario: Empty report
  Given the report has no rows
  When I click "Export CSV"
  Then I see "Nothing to export" and no file downloads
```

Use a checklist format instead if the user's team prefers it or the story is non-behavioral (e.g., a config change).

## INVEST check

Every story should be:
- **I**ndependent — can be built and shipped without another story in the set (where possible)
- **N**egotiable — describes the need, not the implementation
- **V**aluable — delivers value to a user or the business on its own
- **E**stimable — clear enough to size
- **S**mall — fits in a single sprint (ideally 1–3 days)
- **T**estable — acceptance criteria are verifiable

## Splitting patterns (when a story is too big)

- **Workflow steps** — split create / edit / delete / view.
- **Business rule variations** — one story per rule.
- **Happy path first** — defer edge cases to follow-up stories.
- **Data types / platforms** — CSV first, then XLSX; web first, then mobile.
- **Simple → complex** — hard-coded option first, configurable later.
- **Spike** — if unknowns block estimation, create a time-boxed research story.

## Output format

Group by epic, then output a table followed by full story details:

```markdown
## Epic: [Name]

| # | Story | Priority | Size (S/M/L) | Depends on |
|---|-------|----------|--------------|-----------|

### Story 1: [Short title]
**As a** … **I want** … **so that** …

**Acceptance criteria**
- Given … When … Then …

**Notes:** design links, analytics events to fire, out of scope.
```

If the user names a tool (Jira, Linear, GitHub), match its conventions (e.g., Linear titles are imperative: "Add CSV export to Reports"). Offer to output as CSV for bulk import if there are more than ~10 stories.

## Common mistakes to avoid

- Persona is "user" — be specific.
- "So that" restates the "I want" — it must state the *why*.
- Technical tasks disguised as stories ("As a developer I want a database table") — make these tasks/sub-tasks under a real user story instead.
- Acceptance criteria describing UI implementation details instead of observable behavior.
