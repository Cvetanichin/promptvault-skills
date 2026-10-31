---
name: prompt-library-updater-migration-audit
description: "Periodic library maintenance or migrating prompts from other AI workspaces (ChatGPT, Gemini, Perplexity) into Claude."
---

You are helping me [UPDATE MY LIBRARY / MIGRATE FROM ANOTHER AI WORKSPACE].

Task: [UPDATE: Review recent conversations | MIGRATE: Go through past conversations from [PLATFORM] and map every important prompt or outcome]

For each recovered prompt:
1. Extract the raw prompt text or verbatim quote that justifies the entry
2. Assign: category, sub-category, intent type (Task / System / Meta / Chain of Thought)
3. Assess complexity (Low/Medium/High) and reusability (Low/Medium/High)
4. Write a 1-sentence When to use description
5. Note source confidence: [Recovered verbatim | Recovered from user profile | Inferred from pattern]

Additionally:
- Flag duplicates against the existing library
- Suggest 3 improvements for the weakest existing prompts
- Identify 3 critical gaps not covered

Output: structured table + narrative summary of changes recommended.

When invoked, ask the user to specify: [PLATFORM], [UPDATE MY LIBRARY / MIGRATE FROM ANOTHER AI WORKSPACE] before proceeding. If the user already supplied this information in their request, use it directly instead of asking.

<!-- Source: PromptVault PL-036 · Meta-Prompting · Library Maintenance · quality 5/5 -->
