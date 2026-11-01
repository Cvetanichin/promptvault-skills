---
name: data-extraction-cleaning-structuring-pipeline
description: "Use when automating data processing: extracting from a source (CSV/Excel/API/notes), cleaning messy data, structuring unstructured text into tables, or transforming raw datasets for analysis or import into Airtable/Notion/Excel. Produces a five-phase extract-clean-structure-validate-export pipeline with error handling and logging."
---

Build a data processing pipeline with these phases:

Phase 1 — Extract: Read data from [SOURCE: CSV/Excel/API/text notes] using pandas
Phase 2 — Clean: Remove duplicates, fix formatting, standardise field values, handle missing data with [fill/drop/flag] strategy
Phase 3 — Structure: Transform into [DESIRED FORMAT: cleaned table / pivot / database-ready fields / CRM-importable CSV]
Phase 4 — Validate: Flag rows that failed validation with reason column
Phase 5 — Export: Save output to [DESTINATION] with processing summary

For unstructured input (notes/text):
- Extract fields: [FIELD LIST, e.g. name, date, amount, category, tags]
- Output: structured table ready for [Airtable / Notion / Excel / CSV]

Frequency: [Daily / Weekly / On demand]
Error handling: try/except with clear error messages. Include row-level logging. No hardcoded paths.

When invoked, ask the user to specify: [DESTINATION] before proceeding. If the user already supplied this information in their request, use it directly instead of asking.

<!-- Source: PromptVault PL-038 · Data Engineering · Data Processing Pipeline · quality 4/5 -->
