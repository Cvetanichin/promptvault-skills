---
name: schema-driven-structured-output-enforcer
description: "Any AI feature where inconsistent output shapes crash downstream code or parsers. Transforms 40% crash rate to 0%."
---

Design a schema-enforced output system for the following AI task:

Task: [DESCRIBE WHAT THE AI SHOULD EXTRACT OR PRODUCE]
Expected output fields: [LIST FIELDS WITH TYPES, e.g. sentiment: string enum, score: integer 1-10, themes: array of strings]

Deliver:
1. Tool/function schema definition (JSON) — declare every required field with type, enum where applicable, and a precise description the model uses to fill correctly
2. API call pattern using tool_choice to FORCE the model to call your schema (not respond in free text)
3. Response extraction code — reads from tool_calls/tool_use block, already a Python dict, no json.loads needed
4. Validation layer — check types, ranges, and content quality
5. Retry loop — up to 3 attempts, feed previous errors back to the model so it self-corrects
6. Safe fallback — if all retries fail, return a neutral default and log for human review

Key principle: define the shape once as a schema, force the call, read from block.input. Never parse free text.
Target: 0% format-related crashes in production.

When invoked, ask the user to specify: [DESCRIBE WHAT THE AI SHOULD EXTRACT OR PRODUCE] before proceeding. If the user already supplied this information in their request, use it directly instead of asking.

<!-- Source: PromptVault PL-069 · Prompt Engineering · Schema-Driven Output · quality 5/5 -->
