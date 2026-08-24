---
title: "Tool: AI Ark"
type: tool
tags: [tool, data, enrichment, agentic, ai-gtm]
last-updated: 2026-06-12
last-updated-time: 22:30
---

# Tool: AI Ark

> A lead-data search tool [[expert-wesley-hoang]] connects to [[tool-claude-code]] via [[tool-mcp]], so an ICP described in plain English returns an enriched CSV. Referred to in the source transcript as "AIoG".

## What it is

A B2B lead database / search tool with an MCP server. Note: the transcript renders the name inconsistently as "AI Ark" and "AIoG"; treat as one tool pending confirmation of the canonical name.

## What it does (as used)

Connected to Claude as a custom MCP connector, it lets you skip the filter-and-dropdown UI: describe an ICP ("50 CEOs in New York running SaaS companies doing one to five million ARR") and it returns the matching contacts, exported to a CSV with emails and LinkedIn profiles. The agent can then score and flag leads in the same conversation. See [[play-natural-language-icp-list-build]] and [[concept-agentic-sourcing]].

## Setup (from the source)

In Claude: Settings > Connectors > Add custom connector; name it, paste the AI Ark MCP URL, and insert an API key created in AI Ark settings. Restart Claude; the tool then appears as a connector.

## Sources

[[source-wesley-hoang-mcp-lead-lists]].

## Related

[[expert-wesley-hoang]] | [[tool-mcp]] | [[tool-claude-code]] | [[concept-agentic-sourcing]] | [[play-natural-language-icp-list-build]]
