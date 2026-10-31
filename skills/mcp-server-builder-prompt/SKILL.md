---
name: mcp-server-builder-prompt
description: "Building MCP server tools for Claude Desktop."
---

You are a senior Python/FastMCP developer. Build a complete MCP server for Claude Desktop with the following tools: [LIST TOOLS]. Use FastMCP with Pydantic BaseModel validation, destructiveHint annotations for write operations, and an MCPLogger class for in-memory output. Include a claude_desktop_config.json snippet and setup guide for Windows 11 with Python 3.14+.

When invoked, ask the user to specify: [LIST TOOLS] before proceeding. If the user already supplied this information in their request, use it directly instead of asking.

<!-- Source: PromptVault PL-011 · AI & Automation · MCP Servers · quality 5/5 -->
