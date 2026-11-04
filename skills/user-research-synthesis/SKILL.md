---
name: user-research-synthesis
description: Synthesize user interviews, survey responses, support tickets, app reviews, or usability-test notes into themes, insights, and product recommendations. Use when the user shares interview transcripts or notes, survey exports, customer feedback, NPS comments, or asks to find patterns, pain points, jobs-to-be-done, or an affinity map in qualitative data. Also use to draft an interview guide.
---

# User Research Synthesis

Turn raw qualitative data into evidence-backed insights a team can act on.

## Mode A: Synthesize existing data

### 1. Inventory the sources
State what you're working with: number of interviews/responses, participant segments, date range, method. Flag gaps (e.g., "all 8 participants are power users — findings may not generalize to new users").

### 2. Extract observations
Go source by source. Pull out atomic observations — one fact, behavior, pain, or quote each — tagged with the participant/source ID. Keep the participant's own words where possible.

### 3. Cluster into themes (affinity mapping)
Group observations bottom-up. Name each theme as a **statement**, not a topic:
- ❌ "Onboarding"
- ✅ "New admins can't tell which setup steps are required vs. optional"

### 4. Turn themes into insights
For each theme:
- **Insight** — the underlying "why" (need, motivation, mental model).
- **Evidence** — how many sources (e.g., 6/10 participants) + 1–2 representative quotes.
- **Strength** — Strong (many sources, consistent) / Moderate / Weak (signal worth investigating).
- **Implication** — what this means for the product.

### 5. Recommend
Translate insights into opportunities, framed as "How might we…" questions or concrete recommendations, ranked by impact × evidence strength.

### Output format

```markdown
# Research synthesis: [topic]
**Sources:** … **Participants:** … **Caveats:** …

## Key insights (top 3–5)
### 1. [Insight statement]
- **Evidence:** 7/12 participants. "…quote…" (P4)
- **Strength:** Strong
- **Implication:** …

## Other themes
Shorter list of lower-strength or secondary themes.

## Jobs to be done
When [situation], I want to [motivation], so I can [outcome].

## Opportunities / recommendations
| Opportunity | Insight(s) | Evidence strength | Suggested next step |

## Open questions for future research
```

### Rigor rules
- Never invent quotes or counts. Every quote must appear in the source material.
- Distinguish what users **said** from what they **did**; behavior beats stated preference.
- Don't overweight a single vivid anecdote — report frequency.
- Call out contradictions between segments instead of averaging them away.
- Feature requests are data about a need, not a spec — dig to the underlying problem.

## Mode B: Draft an interview guide

When the user is planning research rather than analyzing it:
1. Clarify the research goal and the decision it will inform.
2. Define who to recruit (screener criteria).
3. Write a 30–45 minute guide: warm-up → context/current behavior → specific recent story ("Tell me about the last time you…") → pain points → wrap-up.
4. Use open, non-leading, past-behavior questions. Avoid "Would you use…?" and "Do you like…?" questions.
