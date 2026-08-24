---
title: "Source: Patrick Spychalski -- Clay launched an MCP (rep-facing, not for building)"
type: source
tags: [source, ai-gtm, tool-integration, agentic]
source-title: "The day has come -- Clay just launched an MCP"
source-url: "[LinkedIn post URL not recorded]"
source-author: Patrick Spychalski
source-published: unknown
raw-path: raw/Patrick Spychalski/2.md
last-updated: 2026-06-12
last-updated-time: 22:30
---

# Source: Patrick Spychalski -- Clay launched an MCP (rep-facing, not for building)

> LinkedIn post by [[expert-patrick-spychalski]]. Raw: `raw/Patrick Spychalski/2.md`.

## Summary

[[tool-clay]] launched an [[tool-mcp]], but not the one people expected. It is not for building Clay tables in [[tool-claude-code]]. It is a rep-facing tool that lets sales team members call the workflows you build, more easily. Clay has always held that reps should not use the platform directly and that workflows should be fronted by something friendlier. The MCP is the natural next step: call any Clay workflow from an LLM (currently OpenAI and Claude).

How it works:
1. Connect the Clay app to your LLM of choice.
2. Build a Clay function for a specific task (enrich, qualify, normalise, push to CRM).
3. Enable that function for the MCP.
4. Call it from the command line.

Spychalski's most exciting application: pushing to CRM, sequencers, and the data warehouse. He does not yet trust an agent to operate in his CRM directly, but he does trust a pre-built Clay table that enriches, normalises, and knows the system rules. Best of both worlds: agentically prospect, then push to Clay. See [[play-agentic-prospect-clay-crm-push]].

## Key takeaways

- Clay's MCP exposes built workflows to LLMs for reps, rather than letting agents build tables.
- Use deterministic, rule-aware Clay functions as the safe layer for system-of-record writes.
- Pattern: agentic prospecting up front, governed Clay table for the write.

## Attribution

[[expert-patrick-spychalski]], Co-Founder at The Kiln. Original LinkedIn post.
