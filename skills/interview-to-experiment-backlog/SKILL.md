---
name: interview-to-experiment-backlog
description: Transform raw customer interview notes into a prioritized list of testable experiments.
---

# Interview Notes to Experiment Backlog

## Overview

Convert unstructured customer interview notes into a concise, ranked backlog of experiments. Focus on extracting problems, not solutions, and output actionable hypotheses.

## Process

### Step 1: Extract Pain Points

Scan notes for signals of frustration, workarounds, or unmet needs:

- Direct complaints ("I hate when...")
- Workarounds ("So I just use a spreadsheet instead")
- Frequency markers ("Every single time", "constantly")
- Emotional language ("frustrating", "nightmare", "waste of time")

### Step 2: Cluster Similar Problems

Group related pain points. Use a simple label:

```
[Onboarding] - 3 mentions
- "Took me two weeks to figure out the dashboard"
- "No idea what to do after signup"
- "Had to ask support basic questions"
```

### Step 3: Convert to Experiment Format

Each experiment follows this template:

```
Problem: [One-sentence user problem]
Hypothesis: If we [change], then [outcome] because [reason].
Signal: [How we'll measure success]
Effort: S/M/L
```

### Step 4: Rank by ICE Score

Score each experiment 1-5 on:
- **Impact**: How much pain does this solve?
- **Confidence**: How sure are we this is real?
- **Ease**: How quickly can we test it?

Multiply scores. Sort descending.

## Example Output

```markdown
## Experiment Backlog

| Rank | Problem | Hypothesis | Signal | ICE |
|------|---------|------------|--------|-----|
| 1 | Users abandon onboarding | If we add a 3-step checklist, completion rises 20% because users need clear direction | Onboarding completion rate | 60 |
| 2 | Export takes too long | If we add CSV export, support tickets drop because users need data in spreadsheets | Export usage, ticket volume | 48 |
| 3 | Confusing pricing page | If we simplify tiers to 2 options, signups increase because choice overload causes drop-off | Pricing page conversion | 36 |
```

## Guidelines

- Limit backlog to 5-10 experiments maximum
- One experiment per problem—don't bundle
- Prefer direct quotes as evidence
- Flag experiments with only 1 mention as low confidence
- Output as a markdown table for easy scanning