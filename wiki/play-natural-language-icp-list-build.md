---
title: "Play: Natural-language ICP list build via MCP"
type: play
tags: [play, agentic, ai-gtm, enrichment, signal-based, automation]
last-updated: 2026-06-12
last-updated-time: 22:30
---

# Play: Natural-language ICP list build via MCP

> Connect an agent to a data backend via [[tool-mcp]], describe the ICP in one sentence, and have the agent build, enrich, score, and export the list in a single conversation.

## When to use

Replacing manual filter-and-dropdown list building in a legacy data tool; fast TAM or account-list assembly; when the GTM engineer already works in an agentic CLI.

## Steps

1. **Connect the backend.** Add the data tool as a custom connector / MCP server in the agent. Example: [[expert-wesley-hoang]] adds [[tool-ai-ark]] in Claude settings (Connectors > Add custom connector), pastes the MCP URL, and inserts an API key generated in the tool. See [[source-wesley-hoang-mcp-lead-lists]].
2. **Describe the ICP.** State criteria in plain English: "Grab me 50 CEOs in New York running SaaS companies doing one to five million ARR." More detail yields a better list.
3. **Build the list.** The agent runs the search and pulls the data.
4. **Score and flag.** In the same thread, have the agent score every lead and flag those worth reaching out to first.
5. **Export / route.** Export a CSV with emails and LinkedIn profiles, or (with [[tool-deepline]]) write to Snowflake / Salesforce / HubSpot directly.

## Notes

- Filter on signals before enriching to save credits (see [[concept-waterfall-enrichment]]).
- For governed system-of-record writes, hand off to a rule-aware table rather than letting the agent write directly: see [[play-agentic-prospect-clay-crm-push]].

## Sources

[[source-wesley-hoang-mcp-lead-lists]], [[source-patrick-spychalski-waterfall-claude-code-deepline]].

## Related

[[concept-agentic-sourcing]] | [[tool-mcp]] | [[tool-claude-code]] | [[tool-ai-ark]] | [[tool-deepline]]
