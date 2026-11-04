---
name: experiment-design
description: Design A/B tests and product experiments, write hypotheses, estimate sample size and duration, and interpret experiment results. Use when the user asks to design an A/B test, write an experiment brief, calculate sample size or MDE, decide whether a result is significant, or analyze a test readout.
---

# Experiment Design

Help the user run experiments that produce trustworthy decisions.

## Mode A: Design an experiment

### 1. Hypothesis
Use this format:
> **Because** [evidence/insight], **we believe** [change] **for** [audience] **will cause** [effect on primary metric]. **We'll know it worked when** [metric] changes by [MDE] within [duration].

### 2. Metrics
- **Primary metric** — exactly one; the decision rests on it.
- **Secondary metrics** — help explain *why*.
- **Guardrail metrics** — must not degrade (revenue, latency, unsubscribe rate, errors).

### 3. Design
- **Unit of randomization** — user, account, session, or device. Randomize at the level the change is experienced; use account-level for B2B/collaborative features to avoid contamination.
- **Variants** — control + 1 treatment by default; each extra variant increases required sample size.
- **Allocation** — 50/50 unless there's a risk reason to ramp.
- **Targeting** — who's eligible; exclude anyone who can't be affected.

### 4. Sample size & duration
For a two-sided test on a conversion rate at α = 0.05 and 80% power, a rough per-variant sample size is:

`n ≈ 16 × p(1 − p) / δ²`

where `p` = baseline rate and `δ` = absolute minimum detectable effect.
Example: baseline 10%, detect +1 pp → n ≈ 16 × 0.09 / 0.0001 = 14,400 per variant.

If a code execution tool is available, compute precisely (e.g., `statsmodels.stats.power`). Then: duration = total sample ÷ eligible daily traffic, rounded **up to full weeks** to cover weekly cycles. Minimum 1 week, usually ≤ 4–6 weeks. If the duration is impractical, recommend a larger MDE, a more sensitive metric, or a non-experimental approach.

### 5. Decision rules (pre-registered)
Write down before launch: ship if primary metric is significantly positive and no guardrail is significantly negative; otherwise iterate or kill. Pre-committing prevents post-hoc rationalization.

### Experiment brief output
```markdown
# Experiment: [name]
**Hypothesis:** …
**Primary metric:** … (baseline …, MDE …)
**Guardrails:** …
**Unit / allocation / targeting:** …
**Sample size:** … per variant · **Duration:** … weeks
**Decision rules:** …
**Risks:** novelty effects, network effects, seasonality, instrumentation gaps
```

## Mode B: Interpret results

Work through in order:
1. **Sanity checks** — Sample ratio mismatch (is the split close to the planned allocation? use a chi-square test); did tracking work; did the test run its planned duration?
2. **Primary metric** — effect size, confidence interval, p-value. Report the interval, not just "significant".
3. **Guardrails** — any significant harm?
4. **Segments** — look, but treat segment findings as hypotheses for the next test (multiple comparisons inflate false positives).
5. **Recommendation** — ship / iterate / kill, with reasoning and the practical (not just statistical) significance.

## Pitfalls to flag
- **Peeking** — stopping early when results look good inflates false positives. Use the planned duration or a sequential testing method.
- **Underpowered tests** — "no significant difference" ≠ "no effect".
- **Novelty/primacy effects** — check if the effect decays over time.
- **Too many metrics** — pick one primary; correct for multiple comparisons on the rest.
- **Network effects / interference** — marketplaces and social products may need cluster or switchback designs.
