---
name: grant-pipeline-prioritization-engine
description: "Weekly pipeline review — ranking active grant opportunities by strategic fit, effort-to-value ratio, and readiness."
---

Evaluate and prioritize the following funding opportunities for [ORGANISATION].

Opportunities:
[PASTE LIST: name, funder, deadline, amount, brief description]

Score each on:
- Strategic fit (1-5): alignment with mission, thematic area, geographic scope
- Effort required (1-5 inverse — 5=low effort): proposal complexity, relationship depth needed
- Readiness (1-5): track record match, documentation ready, partnerships in place

Composite score = Fit × (6 - Effort) × Readiness

Output:
1. Ranked table with all scores and composite
2. Top 3 recommendations with rationale
3. 1-2 opportunities to DROP from pipeline and why
4. One quick win (highest readiness, nearest deadline)

When invoked, ask the user to specify: [ORGANISATION] before proceeding. If the user already supplied this information in their request, use it directly instead of asking.

<!-- Source: PromptVault PL-059 · Fundraising · Pipeline Management · quality 5/5 -->
