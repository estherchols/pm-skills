---
name: prioritization
description: Prioritize a list of features, initiatives, bugs, or backlog items using frameworks like RICE, ICE, MoSCoW, Kano, or value-vs-effort, and produce a ranked, defensible recommendation. Use when the user asks what to build next, wants to rank or score a backlog, compare initiatives, build a roadmap order, or mentions RICE/ICE/MoSCoW/Kano.
---

# Prioritization

Help the user rank options and, more importantly, explain *why* — so the result survives a stakeholder review.

## Step 1: Pick the framework

If the user named one, use it. Otherwise pick based on context and say why in one line:

| Situation | Framework |
|-----------|-----------|
| Many items, some data on reach/impact | **RICE** (default) |
| Early stage, little data, need speed | **ICE** |
| Fixed scope/deadline (a release, an MVP) | **MoSCoW** |
| Understanding customer delight vs. table stakes | **Kano** |
| Quick visual for a workshop | **Value vs. Effort 2×2** |

## Step 2: Score

### RICE
`RICE score = (Reach × Impact × Confidence) / Effort`
- **Reach** — # users/events affected per quarter (use a real number).
- **Impact** — 3 = massive, 2 = high, 1 = medium, 0.5 = low, 0.25 = minimal.
- **Confidence** — 100% = data-backed, 80% = some evidence, 50% = gut feel.
- **Effort** — person-months (or person-weeks; be consistent).

### ICE
`ICE = Impact × Confidence × Ease`, each 1–10.

### MoSCoW
Must have / Should have / Could have / Won't have (this time). Rule of thumb: Musts ≤ 60% of capacity.

### Kano
Classify each item: Basic (expected; absence causes dissatisfaction), Performance (more is better), Delighter (unexpected; creates delight), Indifferent, Reverse.

### Value vs. Effort
Quick wins (high value/low effort) → Big bets (high/high) → Fill-ins (low/low) → Money pits (low/high, avoid).

## Step 3: Handle missing data honestly

- If the user didn't give numbers, propose estimates, **mark each one as an estimate**, and lower Confidence accordingly.
- Ask for the 1–2 inputs that would most change the ranking rather than every missing value.

## Step 4: Output

```markdown
## Recommendation
Top 3 in order, one sentence each on why.

## Scoring table
| Rank | Item | Reach | Impact | Confidence | Effort | Score | Notes |
(sorted by score)

## Sensitivity
Which items would swap rank if a key estimate were wrong? e.g. "If Effort for X is 2× higher, Y overtakes it."

## What we're not doing (and why)
Bottom items with a short rationale — this is what stakeholders will push on.

## Assumptions
List every estimated input.
```

## Judgment beyond the formula

After scoring, sanity-check and call out where the formula misleads:
- **Strategic fit** — does a lower-scored item unlock a strategic goal or a big customer?
- **Dependencies** — does something need to come first regardless of score?
- **Risk reduction** — small, uncertain items may be worth doing early to learn.
- **Cost of delay** — compliance deadlines, seasonal windows, contract commitments.

State explicitly when you'd override the score and why. Frameworks inform decisions; they don't make them.
