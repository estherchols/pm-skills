---
name: prd-writer
description: Write a product requirements document (PRD) or one-pager for a feature or product. Use when the user asks for a PRD, product spec, feature spec, requirements doc, one-pager, or "write up this feature idea", or pastes rough notes about a feature and wants them turned into a structured spec.
---

# PRD Writer

Turn a feature idea, rough notes, or a problem statement into a crisp PRD that an engineering, design, and leadership audience can all act on.

## Step 1: Gather context (ask only what's missing)

Before drafting, make sure you know these. Infer from what the user gave you; ask in one batch only for gaps that would materially change the doc:

1. **Problem** — Who has the problem, and what evidence shows it's real (data, tickets, quotes)?
2. **Target user** — Which segment/persona? Be specific ("admins at 50–500 seat B2B accounts", not "users").
3. **Goal** — What business or user outcome changes if this ships?
4. **Constraints** — Deadline, platform, team size, dependencies, compliance.
5. **Format** — Full PRD or a one-pager? Default to full PRD; use one-pager if the user says "quick", "lightweight", or "one-pager".

If the user just wants a draft, proceed with clearly marked assumptions (`> **Assumption:** ...`) rather than blocking on questions.

## Step 2: Draft using this structure

```markdown
# [Feature name] — PRD
**Author:** · **Status:** Draft · **Last updated:** [date]

## TL;DR
2–3 sentences: the problem, the proposed solution, and the expected impact.

## Problem
- What's broken or missing, for whom, and how we know (cite evidence).
- Cost of not solving it.

## Goals & Non-goals
**Goals** (measurable): e.g. "Increase week-1 activation from 32% → 40%".
**Non-goals**: things a reader might assume are in scope but are not.

## Target users & use cases
Persona(s) + 3–5 key use cases / jobs-to-be-done.

## Proposed solution
- Core user flow (numbered steps).
- Key screens/states described in words (or link to designs).
- What changes for existing users.

## Requirements
| ID | Requirement | Priority (P0/P1/P2) | Notes |
|----|-------------|---------------------|-------|
P0 = launch blocker, P1 = should have, P2 = nice to have.

## Success metrics
- **Primary metric** (one): definition, baseline, target, timeframe.
- **Secondary metrics**.
- **Guardrail metrics**: what must NOT get worse (latency, churn, support volume).

## Risks & open questions
| Risk / question | Impact | Mitigation / owner |

## Launch plan & milestones
Phases (alpha → beta → GA), rollout %, dates or relative timing.

## Appendix
Research links, data, alternatives considered (and why rejected).
```

**One-pager variant:** TL;DR, Problem, Solution, Success metric, Risks, Ask — max ~1 page.

## Step 3: Quality check before returning

- [ ] Problem is stated before solution, and backed by evidence or a flagged assumption.
- [ ] Every goal is measurable (number + timeframe).
- [ ] Non-goals exist and are meaningful.
- [ ] Requirements are testable — an engineer could write an acceptance test for each.
- [ ] Exactly one primary success metric, plus at least one guardrail.
- [ ] No solution-speak in the Problem section.
- [ ] Open questions have owners.

## Writing guidance

- Be concrete: numbers, named segments, real examples. Cut adjectives like "seamless" and "intuitive".
- Write for skimmers: short paragraphs, bullets, tables.
- Separate facts, assumptions, and opinions explicitly.
- If the user's idea has an obvious weakness (unclear user, no evidence, unmeasurable goal), say so in the Open Questions section rather than papering over it.
