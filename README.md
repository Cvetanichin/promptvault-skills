# PromptVault Skills

78 ready-to-use [Agent Skills](https://code.claude.com/docs/en/skills.md) for
Claude Code, Cursor, and GitHub Copilot, curated from the
[PromptVault](https://github.com/Cvetanichin/PromptVault) prompt library. Each
skill is a self-contained instruction set your agent can invoke by name — no app,
no dependencies, just drop the folders into your project.

## Quick install

```bash
# Claude Code
git clone <this-repo-url>
cp -r promptvault-skills/skills/* /path/to/your-project/.claude/skills/
```

Then start (or restart) `claude` in your project. Using Cursor or GitHub Copilot
instead? Same skills, just a different folder — see [INSTALL.md](INSTALL.md) for
the Cursor (`.cursor/skills/`) and Copilot (`.github/skills/`) paths, Windows
instructions, installing a single skill, and troubleshooting.

## What's in here

General-purpose prompt-engineering, automation, research, writing, and productivity
skills, plus a set of reusable fundraising and organizational-development prompts
for civil society organizations (CSOs/NGOs) — curated from PromptVault's library.
Left out: anything personalized to the original author's own name, brand, or
workspace setup — this pack is for any project, not a specific person.

| Category | Skills |
|---|---|
| Prompt Engineering | 10 |
| System Prompt (personas/modes) | 9 |
| AI & Automation | 8 |
| Research & Analysis | 7 |
| Fundraising | 6 |
| Meta-Prompting | 6 |
| Organizational Development | 5 |
| Workspace & Productivity | 4 |
| Clarification | 3 |
| Data Engineering | 3 |
| Project Management | 3 |
| Rephrasing | 3 |
| Summarization | 3 |
| Versioning | 3 |
| Capacity Building | 2 |
| Vibe Coding / Product | 2 |
| Communication | 1 |

Full catalog with descriptions: [INSTALL.md § Catalog](INSTALL.md#catalog).

## License

See [LICENSE](LICENSE).
