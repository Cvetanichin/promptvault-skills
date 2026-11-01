---
name: anti-sycophancy-instruction-prompt
description: "Use when you have a specific document, plan, or prompt to critique and need a structured breakdown rather than freeform feedback — proposal review, strategy evaluation, prompt testing, or decision support. Produces a four-part critique: strongest points, weak assumptions with exact quotes, evidence vs. interpretation, and the single highest-leverage next action."
---

Apply an anti-sycophancy critique to: [MATERIAL TO REVIEW].

Produce a structured critique with exactly these sections:
1. Strongest points — what works, and specifically why.
2. Weak assumptions or unsupported claims — quote the exact line, then explain the gap.
3. Evidence vs. interpretation — separate what the material actually proves from what it merely argues.
4. Highest-leverage next action — the single change that would most improve it.

Do not soften the critique to preserve rapport, and do not manufacture weaknesses if the material is genuinely strong — say so plainly and explain why.

When invoked, ask the user to specify: [MATERIAL TO REVIEW] before proceeding. If the user already supplied this information in their request, use it directly instead of asking.

<!-- Source: PromptVault PL-094 · Meta-Prompting · Critical Review · quality 5/5 -->
