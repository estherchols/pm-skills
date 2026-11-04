---
name: launch-plan
description: Create a go-to-market or product launch plan, including launch tiering, rollout phases, cross-functional checklist, messaging, and release notes. Use when the user asks for a launch plan, GTM plan, rollout plan, launch checklist, release notes, announcement copy, or "how should we ship this".
---

# Launch Plan

Plan a launch sized to its importance, with every function knowing what to do and when.

## Step 1: Tier the launch

Ask or infer, then state the tier and why:

| Tier | What it is | Typical motion |
|------|-----------|----------------|
| **Tier 1** | New product, major feature, pricing change; affects positioning | Full GTM: press, event, campaign, sales enablement, 6–8 weeks of prep |
| **Tier 2** | Significant feature for an existing audience | Blog post, email to relevant segment, in-app announcement, enablement doc, 2–4 weeks |
| **Tier 3** | Improvement or small feature | Changelog / release notes, in-app tooltip, support macro, ~1 week |

## Step 2: Define the essentials

- **Audience** — which segments get it, and which are told about it.
- **Positioning** — one-sentence value proposition in customer language: "[Product] now lets [audience] [do X] so they can [benefit]."
- **Goals** — launch success metrics (adoption, activation, pipeline, press) with targets.
- **Launch date** and the go/no-go decision date.

## Step 3: Rollout strategy

Recommend phases appropriate to risk:
1. **Internal dogfood** — employees.
2. **Alpha / design partners** — 5–20 friendly customers, high touch.
3. **Beta** — opt-in or % rollout behind a feature flag; monitor guardrails.
4. **GA** — 100% plus announcement.

For each phase: entry criteria, exit criteria (metrics/quality bars), rollback plan, owner.

## Step 4: Cross-functional checklist

Generate a checklist organized by team, each item with an owner and due date relative to launch (T-minus):

- **Product** — PRD final, success metrics instrumented, dashboards live, go/no-go meeting.
- **Engineering** — feature flag, load/perf testing, monitoring and alerts, rollback tested.
- **Design** — final assets, in-app education (tooltips, empty states).
- **Marketing** — messaging doc, blog post, email, social, website updates, screenshots/video.
- **Sales / CS** — enablement session, FAQ, battlecard updates, pricing/packaging confirmed.
- **Support** — help-center articles, macros, escalation path, staffing for launch week.
- **Legal / compliance** — privacy review, terms updates, regional restrictions.
- **Post-launch** — T+1 week and T+30 day metric reviews, feedback collection, retro.

Scale the checklist to the tier — a Tier 3 launch should not get a 40-item list.

## Step 5: Output

```markdown
# Launch plan: [feature] — Tier [n]
**Launch date:** … · **Go/no-go:** … · **DRI:** …

## Summary & positioning
## Audience & goals
## Rollout phases
| Phase | Audience | Dates | Exit criteria | Rollback trigger |
## Checklist by team
| Item | Owner | Due (T-minus) | Status |
## Messaging
Headline, 3 key benefits, proof points, FAQ.
## Risks & mitigations
## Post-launch review plan
```

## Release notes / announcement copy

When asked for copy: lead with the customer benefit, not the feature name; one short paragraph + 2–3 bullets; include how to access it and a link to docs. Offer variants for changelog, email, and in-app (≤ 140 characters).
