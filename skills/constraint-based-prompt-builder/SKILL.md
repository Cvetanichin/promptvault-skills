---
name: constraint-based-prompt-builder
description: "High-precision prompts for recurring high-stakes tasks."
---

Design a prompt for: [DESCRIBE TASK]
Apply these constraint layers:
- Role constraint: who the model should be
- Output format constraint: exact structure required
- Scope constraint: what to include AND exclude
- Quality constraint: self-evaluation criteria
- Failure mode constraint: what errors to avoid
Present the final prompt with each constraint commented.

When invoked, ask the user to specify: [DESCRIBE TASK] before proceeding. If the user already supplied this information in their request, use it directly instead of asking.

<!-- Source: PromptVault PL-053 · Prompt Engineering · Constraint-Based Design · quality 5/5 -->
