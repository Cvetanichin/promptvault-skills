---
name: self-evaluating-meta-prompt-template
description: "High-stakes outputs: proposals, M&E frameworks, reports."
---

Generate [OUTPUT TYPE] for [CONTEXT]. Structure: (1) Produce the output. (2) Define 5 quality criteria. (3) Self-evaluate each criterion score 1-5. (4) Identify the 2 weakest areas. (5) Revise the output. (6) Explain the key changes made.

When invoked, ask the user to specify: [CONTEXT], [OUTPUT TYPE] before proceeding. If the user already supplied this information in their request, use it directly instead of asking.

<!-- Source: PromptVault PL-017 · Meta-Prompting · Self-Evaluation · quality 5/5 -->
