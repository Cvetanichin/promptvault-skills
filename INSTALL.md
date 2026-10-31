# Installing PromptVault Skills

This repo contains 67 [Claude Code skills](https://code.claude.com/docs/en/skills.md)
— each one a `skills/<skill-name>/SKILL.md` folder. A skill is just a markdown file
with a short YAML header; Claude Code discovers it automatically once it's placed in
the right location. There's nothing to build, install, or configure beyond copying
files.

## Prerequisite

[Claude Code](https://claude.com/claude-code) installed and working in your project.

## Install all skills into one project

```bash
# macOS / Linux
git clone <this-repo-url>
cp -r promptvault-skills/skills/* /path/to/your-project/.claude/skills/
```

```powershell
# Windows (PowerShell)
git clone <this-repo-url>
Copy-Item -Recurse promptvault-skills\skills\* C:\path\to\your-project\.claude\skills\
```

If your project doesn't have a `.claude/skills/` folder yet, create it first — the
commands above will create it for you as part of the copy.

## Install skills for every project (not just one)

Copy into your personal skills folder instead of a specific project's:

```bash
cp -r promptvault-skills/skills/* ~/.claude/skills/
```

Skills placed here are available in **every** Claude Code session on your machine,
regardless of which project you're in.

## Install a single skill

Copy just the one folder you want:

```bash
cp -r promptvault-skills/skills/mcp-server-builder-prompt /path/to/your-project/.claude/skills/
```

## Verify it worked

1. Start (or restart) `claude` from the project directory you copied into.
2. Ask Claude something like *"what skills do you have available?"*, or invoke one
   directly by name (e.g. type `/mcp-server-builder-prompt` in the prompt).
3. If a skill doesn't show up, run `/doctor` inside Claude Code — it reports any
   skill whose file failed to load (usually a YAML formatting issue).

**One cold-start note:** if `.claude/skills/` did not exist in your project *before*
you started your current Claude Code session, the newly created folder won't be
picked up automatically — run `/reload-skills`, or just start a fresh `claude`
session in that directory. This only matters the very first time you add skills to
a project; after that, new or edited skills take effect immediately in the current
session.

## Sharing with your team

`.claude/skills/` is a normal directory — commit it to your project's git repo like
any other file, and everyone on the team gets the same skills the next time they
pull.

## Updating

Re-run the same `cp -r` command after pulling the latest version of this repo — it
will overwrite the skill folders with the newer versions. Your own custom skills
(anything not from this pack) are untouched since they live in differently-named
folders.

## Uninstalling

Delete the folder(s) from `.claude/skills/` (or `~/.claude/skills/`). There's no
other state to clean up.

---

## Catalog

All 67 skills, grouped by category. The `Skill` column is the exact name you invoke
(e.g. `/mcp-server-builder-prompt`).
### Prompt Engineering (10)

| Skill | Description |
|---|---|
| `adversarial-test-case-generator` | Stress-testing any prompt before deploying in a library or automated workflow. |
| `ai-output-consistency-tester` | Before shipping any AI feature to production — or when a system prompt has been changed. Proves consistency programmatically with assertion-based scoring. |
| `constraint-based-prompt-builder` | High-precision prompts for recurring high-stakes tasks. |
| `few-shot-example-generator` | Upgrading any prompt by adding concrete examples. |
| `multi-step-delegation-pipeline-builder` | Any task where a single mega-prompt produces shallow or generic output. One prompt, one cognitive mode — quality multiplies when steps specialize. |
| `output-format-specifier` | Eliminating format inconsistency from any prompt. |
| `persona-enriched-task-prompt-builder` | Upgrading generic prompts with rich persona context. |
| `schema-driven-structured-output-enforcer` | Any AI feature where inconsistent output shapes crash downstream code or parsers. Transforms 40% crash rate to 0%. |
| `three-layer-system-prompt-constructor` | Any AI feature, assistant, or recurring workflow where consistent tone, policy-compliance, and predictable behaviour matter. Vague prompts → improvised behavio… |
| `zero-shot-task-decomposer` | Converting a large complex task into a chain of smaller precise prompts. |

### AI & Automation (8)

| Skill | Description |
|---|---|
| `ai-workflow-automation-designer` | Designing AI-powered automation for recurring tasks — monthly system upgrades, new tool integrations, or scaling manual workflows. |
| `cso-workflow-automation-blueprint-make-com-n8n` | When designing a specific workflow automation for an NGO or consultancy, such as partner update aggregation, grant tracking, report drafting, or meeting follow… |
| `digital-hygiene-agent-prompt` | Automated local/Drive file management. |
| `google-workspace-automation-local-cloud-integration-architecture` | Use when setting up or improving automations between local files and Google Workspace (Drive, Gmail, Calendar, Keep). Produces a connected architecture with wo… |
| `mcp-server-builder-prompt` | Building MCP server tools for Claude Desktop. |
| `multi-source-partner-update-aggregation-system` | When building an automation system for a CSO network, consortium, or large NGO that receives updates from multiple partners and needs one clean reporting view. |
| `powershell-file-organizer` | Windows file organization and Drive mirroring. |
| `react-dashboard-connector` | Connecting a Python backend pipeline to a React frontend. |

### Research & Analysis (7)

| Skill | Description |
|---|---|
| `ai-driven-growth-experiment-design-insight-hypothesis-experiment-workflo` | Use when designing structured growth experiments from user feedback or community data. Useful for product teams, NGO programme designers testing interventions,… |
| `ai-driven-root-cause-analysis-for-ngo-performance-decline` | When a key performance indicator is underperforming and the team needs to diagnose why before donor reporting or adaptive management decisions. |
| `comprehensive-research-summary` | In-depth understanding for proposals, reports, or strategic planning. |
| `constitutional-court-research-prompt` | Legal research on Constitutional Court jurisprudence in Western Balkans. |
| `driver-tree-root-cause-analysis-pack` | When a key performance indicator is declining and you need to move from data observation to structured root cause hypotheses to management recommendations — in… |
| `rapid-evidence-review-prompt` | Background research during proposal development or evaluation prep. |
| `variance-bridge-financial-analysis-pack` | When gross margin or profitability is deteriorating and you need to decompose the financial variance into its drivers, link to operational causes, and communic… |

### Workspace & Productivity (4)

| Skill | Description |
|---|---|
| `airtable-notion-database-architecture` | Setting up a project management, CRM, or M&E database in Airtable or Notion — system design phase. |
| `design-unified-google-drive-notion-workspace-two-domain-structure` | Use when setting up or redesigning a dual-domain personal workspace in Google Drive + Notion — especially for solo civil society/NGO professionals who also do… |
| `notion-task-meeting-creator` | Creating structured Notion entries via Claude integration. |
| `weekly-project-status-recap-workspace-scan` | Weekly workspace scan that identifies all active projects, gathers recent activity from the past 1-2 weeks, and produces a concise project recap per project co… |

### Meta-Prompting (6)

| Skill | Description |
|---|---|
| `anti-sycophancy-instruction-prompt` | At the start of any session where honest critique matters: proposal review, strategy evaluation, product planning, prompt testing, or decision support. |
| `dual-format-output-packager` | Any deliverable that needs to exist in both narrative (Word/PDF) and tabular (Excel/Notion) formats — standard for donor handoffs and workspace documentation. |
| `expert-role-activation-prompt` | Opening complex task sessions. |
| `prompt-library-updater-migration-audit` | Periodic library maintenance or migrating prompts from other AI workspaces (ChatGPT, Gemini, Perplexity) into Claude. |
| `self-evaluating-meta-prompt-template` | High-stakes outputs: proposals, M&E frameworks, reports. |
| `structured-output-chain-of-thought` | Complex structured deliverables where quality control matters. |

### Data Engineering (3)

| Skill | Description |
|---|---|
| `data-analysis-and-impact-dashboard-agent-vintage-pastels` | Use as a system prompt for an AI data analysis agent that processes CSV/Excel/PDF project files and generates interactive Plotly dashboards using the Vintage P… |
| `data-extraction-cleaning-structuring-pipeline` | Automating data processing: extracting from source, cleaning messy data, structuring unstructured input (notes/text), or transforming raw datasets for analysis… |
| `google-sheets-excel-data-consolidation-script` | Consolidating data spread across multiple spreadsheet tabs or files — common in M&E data entry, expense tracking, beneficiary registers, or multi-project repor… |

### Project Management (3)

| Skill | Description |
|---|---|
| `phased-implementation-plan-generator-for-cso-projects` | When launching a new project, system, workflow automation, or organizational initiative that needs clear phases and milestones. |
| `stakeholder-mapping-engagement-plan` | Project planning and proposal development. |
| `work-breakdown-structure-generator` | Start of a project or proposal to plan tasks. |

### Rephrasing (3)

| Skill | Description |
|---|---|
| `audience-adaptive-rewriter` | Adapting reports, proposals, or communications for a specific reader. |
| `register-shifter-formal-to-plain` | Making donor reports or M&E documents accessible to non-specialist audiences. |
| `simplifier-plain-language-converter` | Creating beneficiary-facing communications or accessible public documents. |

### Summarization (3)

| Skill | Description |
|---|---|
| `cross-document-comparative-summary` | Comparing donor reports, research studies, or proposal evaluations side by side. |
| `executive-summary-generator` | Executive summaries for donor reports, board briefs, or proposal annexes. |
| `multi-level-summary-builder` | Same content in different formats for different audiences. |

### Versioning (3)

| Skill | Description |
|---|---|
| `document-version-comparator` | Reviewing revised proposals, report drafts, or policy documents between versions. |
| `iterative-refinement-protocol` | Refined, polished output through 3 iterations. |
| `prompt-version-controller` | Systematically improving and version-controlling prompts. |

### Capacity Building (2)

| Skill | Description |
|---|---|
| `ai-literacy-workshop-prompt` | AI upskilling sessions within CSO/NGO settings. |
| `training-programme-module-builder` | Designing full training programmes or individual session modules for CSOs, NGOs, or partner organisations. |

### Vibe Coding / Product (2)

| Skill | Description |
|---|---|
| `lean-no-code-product-constrainer` | Opening any product design or build session — sets the default constraints toward lightweight, fast, no-code-first solutions. |
| `mvp-product-specification-builder` | Turning a rough product idea into a testable MVP specification — for digital tools, internal systems, AI-powered apps, or civic tech prototypes. |

### Communication (1)

| Skill | Description |
|---|---|
| `feature-to-benefit-copywriter` | Rewriting technical or operational descriptions as compelling, benefit-led copy for donor reports, grant applications, website content, or social media. |

### Clarification (3)

| Skill | Description |
|---|---|
| `ambiguity-detector-question-generator` | Start of complex or high-stakes tasks to prevent misinterpretation. |
| `concept-explainer-three-audiences` | Communicating the same idea to multiple stakeholders. |
| `requirements-clarification-protocol` | Tackling unfamiliar or underspecified tasks. |

### System Prompt (9)

| Skill | Description |
|---|---|
| `ai-prompt-engineer-mode` | AI Prompt Engineer Mode |
| `anti-sycophancy-critic` | Anti-Sycophancy Critic |
| `balanced-feedback-mode` | Balanced Feedback Mode |
| `data-privacy-protocol` | Data Privacy Protocol |
| `decision-useful-output-standard` | Decision-Useful Output Standard |
| `lean-product-builder-mode` | Lean Product Builder Mode |
| `python-fastmcp-dev` | Python / FastMCP Dev |
| `researcher-mode` | Researcher Mode |
| `strategic-minimalist-writer` | Strategic Minimalist Writer |

