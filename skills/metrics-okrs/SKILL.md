---
name: metrics-okrs
description: Define product metrics, North Star metrics, metric trees, KPIs, and OKRs, or critique existing ones. Use when the user asks how to measure success, what metrics to track, define a North Star, write or review OKRs, build a KPI dashboard spec, set goals for a quarter, or diagnose why a metric moved.
---

# Metrics & OKRs

Help the user measure what matters and set goals that drive the right behavior.

## Mode A: Define metrics for a product or feature

1. **Start from value.** What does a user get from the product? The best metrics capture that value being delivered.
2. **North Star metric** — one metric that reflects customer value and predicts long-term business success. Good North Stars are:
   - Value-based (not vanity: avoid raw signups or pageviews).
   - Leading (moves before revenue does).
   - Actionable by the team.
   - Examples: weekly active teams sending ≥1 message (collaboration tool), nights booked (marketplace), files edited per week (editor).
3. **Metric tree** — decompose the North Star into input metrics the team can directly influence:
   ```
   Weekly active teams
   ├── New teams activated  (acquisition × activation rate)
   ├── Retained teams       (prior week actives × retention rate)
   └── Resurrected teams
   ```
4. **For a feature**, use a layered set:
   - **Adoption** — % of eligible users who try it.
   - **Engagement** — frequency/depth of use.
   - **Outcome** — did it achieve the goal (task success, time saved, conversion)?
   - **Guardrails** — what must not degrade (performance, churn, support tickets, other features' usage).
5. **Specify each metric precisely:** name, exact definition (numerator/denominator, time window, filters), data source, owner, current baseline, target. Ambiguous definitions cause most metric arguments.

Frameworks to draw on when helpful: AARRR (pirate metrics) for funnels, HEART (Happiness, Engagement, Adoption, Retention, Task success) for UX.

## Mode B: Write OKRs

**Objective** — qualitative, inspiring, time-bound direction. **Key Results** — 2–4 measurable outcomes that prove the objective was achieved.

```markdown
**Objective:** Make onboarding effortless for new admins
- KR1: Increase week-1 activation from 32% → 45%
- KR2: Reduce median time-to-first-value from 3 days → 1 day
- KR3: Cut onboarding-related support tickets by 30%
```

Rules:
- KRs are **outcomes, not outputs**. "Launch the new setup wizard" is a task/initiative, not a KR.
- Every KR has a baseline and a target number.
- Ambitious but plausible — ~70% achievement is typical for stretch OKRs.
- 3–5 objectives max per team per quarter.
- Include a guardrail where a KR could be gamed (e.g., activation up but quality down).

## Mode C: Critique existing metrics/OKRs

Check for and flag: vanity metrics, outputs disguised as outcomes, missing baselines, unmeasurable KRs, too many objectives, metrics the team can't influence, missing guardrails, and incentives that could be gamed. Rewrite each problematic item.

## Mode D: Diagnose a metric change

When a metric moved unexpectedly, work through: (1) is it real — data pipeline, tracking, or definition changes? (2) seasonality/external events, (3) segment breakdown (platform, geo, new vs. existing, plan), (4) internal changes (releases, experiments, pricing, marketing), (5) decompose via the metric tree to find which input moved. Propose the specific queries to run.
