---
name: ai-output-consistency-tester
description: "Before shipping any AI feature to production — or when a system prompt has been changed. Proves consistency programmatically with assertion-based scoring."
---

Design a consistency testing protocol for the following AI prompt or system:

Prompt / system to test: [PASTE THE PROMPT OR DESCRIBE THE SYSTEM]
Behaviours that must be consistent across every run: [LIST 4-6 SPECIFIC ASSERTIONS]

For each assertion, write a testable check:
Assertion 1: [Does the response mention X?] → check: look for keyword/phrase Y in output
Assertion 2: [Does it avoid inventing Z?] → check: absence of pattern P
Assertion 3: [Does it always include escalation path?] → check: presence of contact/phrase
...

Testing protocol:
1. Send the same test question N times (recommended: 10-20 runs)
2. Score each response against each assertion (pass/fail)
3. Calculate consistency score per assertion: (passes / N) × 100%
4. Flag any assertion below 90% as FRAGILE — system prompt needs tightening on that dimension

Output format:
| Assertion | Score (%) | Fragile? | Fix suggestion |

Key principle: a score below 90% means real users will see inconsistent behaviour. Ship nothing without this test. Use it after every prompt change.

When invoked, ask the user to specify: [LIST 4-6 SPECIFIC ASSERTIONS], [PASTE THE PROMPT OR DESCRIBE THE SYSTEM] before proceeding. If the user already supplied this information in their request, use it directly instead of asking.

<!-- Source: PromptVault PL-072 · Prompt Engineering · Consistency Testing · quality 4/5 -->
