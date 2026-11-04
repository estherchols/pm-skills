---
name: competitive-analysis
description: Research and analyze competitors for a product or feature, producing a feature comparison matrix, positioning map, SWOT, and strategic recommendations. Use when the user asks for competitive analysis, competitor research, market landscape, "how do we compare to X", battlecards, differentiation, or positioning.
---

# Competitive Analysis

Produce a decision-oriented view of the competitive landscape — not just a feature list.

## Step 1: Frame the question

Clarify (or infer) the decision this analysis supports, because it changes what matters:
- Entering a new market? → landscape + gaps.
- Building a specific feature? → how competitors solve that job.
- Sales enablement? → battlecards with objection handling.
- Pricing? → packaging and price points.

## Step 2: Identify competitors

Include three tiers:
- **Direct** — same product, same customer.
- **Indirect** — different product, same job (including spreadsheets, agencies, "do nothing").
- **Emerging** — new entrants or adjacent players likely to move in.

Aim for 3–6 total; more dilutes the analysis.

## Step 3: Research

If web search/fetch tools are available, use them. Prioritize primary sources: pricing pages, product docs, changelogs, release notes, job postings (signal of strategy), and review sites (G2, Capterra, App Store) for real user sentiment. **Cite a source for every factual claim** and note the date checked. If you can't verify something, mark it "unverified" — never guess at pricing or features.

If no tools are available, work from what the user provides and your general knowledge, and say clearly that facts should be verified.

## Step 4: Analyze

### Feature / capability matrix
| Capability | Us | Comp A | Comp B | Comp C |
Use ✅ / ◐ (partial) / ❌ / ? (unknown). Choose capabilities that matter to the target customer, not every feature.

### Positioning
Describe each competitor's target customer, core value proposition, and pricing model in one line each. Optionally suggest a 2×2 positioning map with the two axes that best separate the players (e.g., "self-serve ↔ sales-led" × "point solution ↔ platform").

### SWOT (for the user's product relative to the field)
Strengths, Weaknesses, Opportunities, Threats — each item specific and tied to a competitor where relevant.

### What users say
Top praise and complaints about each competitor from reviews — these reveal openings.

## Step 5: Output

```markdown
# Competitive analysis: [market/feature] — [date]

## Summary
3–5 bullets: where we win, where we lose, biggest threat, biggest opportunity.

## Landscape
## Feature matrix
## Positioning
## SWOT
## Strategic recommendations
1–3 concrete moves (differentiate on X, close gap on Y, don't compete on Z).

## Sources
```

**Battlecard variant** (for sales): per competitor — when we win, when we lose, their pitch, our counter, landmines to set, top objections + responses. One page each.

## Guardrails
- Be fair to competitors; an analysis that says "we're better at everything" is useless.
- Separate verified facts from inference.
- Feature parity is rarely a strategy — focus on the jobs customers hire the product for.
