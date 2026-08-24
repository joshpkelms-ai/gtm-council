---
title: "Tool: MCP (Model Context Protocol)"
type: tool
tags: [tool, tool-integration, agentic, ai-gtm, automation]
last-updated: 2026-06-13
last-updated-time: 10:30
---

# Tool: MCP (Model Context Protocol)

> The open protocol that connects LLM agents to external tools and data. In GTM, it is the wire that turns data vendors and workflow platforms into things an agent can call from a conversation.

## What it is

Model Context Protocol: a standard for exposing tools, data, and workflows to LLM agents (Claude, OpenAI). In this corpus it appears as the connective layer that makes [[concept-agentic-sourcing]] possible. A server can offer three capability types: **resources** (readable data), **tools** (callable functions, with user approval), and **prompts** (templates). Because it is a protocol, any client can call any server, which is the whole point: build once, reuse everywhere. See [[source-mcp-reference-docs]]. Sibling format: [[tool-agent-skills]] (a documented procedure for using those tools).

## Position in the corpus

- **Data backends as connectors.** [[expert-wesley-hoang]] connects [[tool-claude-code]] to [[tool-ai-ark]] via a custom MCP connector to build lead lists from one sentence. See [[source-wesley-hoang-mcp-lead-lists]] and [[play-natural-language-icp-list-build]].
- **Workflow platforms going rep-facing.** [[tool-clay]]'s MCP lets reps call built Clay functions from an LLM rather than building tables. The Functions feature is explicitly designed to be callable from Claude, ChatGPT, and Glean over MCP, making each function a unit of GTM logic any agent can invoke. See [[source-patrick-spychalski-clay-mcp]], [[source-clay-functions-course]], [[concept-gtm-functions]], and [[play-agentic-prospect-clay-crm-push]].
- **Signal layers.** Practitioners layer a B2B-signals MCP on top of enrichment to filter before spending credits. See [[concept-waterfall-enrichment]].
- **Building GTM servers.** When no public MCP exists for a GTM tool, practitioners build custom servers (e.g. LinkedIn-profile tools), or spin them up no-code via [[tool-cargo]] to prototype and ship fast. The current sweet spot is prototyping and shaping workflows, not ripping out existing API layers. See [[source-cargo-mcp-gtm-workshop]].
- **Authenticated action.** Connectors extend agents from reading public data to acting under an account (Notion, GitHub, Slack), the same authenticated-write caution [[expert-patrick-spychalski]] applies to CRM writes. See [[source-mcp-reference-docs]].

## Related

[[tool-claude-code]] | [[tool-clay]] | [[tool-ai-ark]] | [[tool-deepline]] | [[tool-cargo]] | [[tool-agent-skills]] | [[concept-agentic-sourcing]] | [[play-natural-language-icp-list-build]] | [[play-agentic-prospect-clay-crm-push]] | [[source-mcp-reference-docs]] | [[source-cargo-mcp-gtm-workshop]]
