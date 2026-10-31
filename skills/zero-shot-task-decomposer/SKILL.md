---
name: zero-shot-task-decomposer
description: "Converting a large complex task into a chain of smaller precise prompts."
---

Break down the following complex task into a step-by-step zero-shot prompt sequence: [PASTE COMPLEX TASK]
For each step: (1) Write a self-contained prompt, (2) State what input it requires and what output it produces, (3) Indicate if the output feeds the next step. Present as a numbered chain.

When invoked, ask the user to specify: [PASTE COMPLEX TASK] before proceeding. If the user already supplied this information in their request, use it directly instead of asking.

<!-- Source: PromptVault PL-052 · Prompt Engineering · Zero-Shot Decomposition · quality 4/5 -->
