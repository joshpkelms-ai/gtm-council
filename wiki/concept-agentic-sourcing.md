---
title: "Concept: Agentic sourcing (natural-language list building)"
type: concept
tags: [concept, agentic, ai-gtm, enrichment, automation, signal-based]
last-updated: 2026-06-12
last-updated-time: 22:30
---

# Concept: Agentic sourcing

> Describe your ICP in plain English and an agent builds, enriches, and scores the list, collapsing the filter-and-dropdown UI of legacy data tools into one conversation.

## The shift

Building a lead list used to mean an hour of clicking through filters and hoping you picked the right criteria. With an agent connected to a data backend via [[tool-mcp]], you state the ICP -- "50 CEOs in New York running SaaS companies doing one to five million ARR" -- and the agent runs the search, pulls the data, exports a CSV with emails and LinkedIn profiles, and can score and flag the leads worth prioritising, all in one thread. No tab switching, no manual filtering.

## Where it shows up

- [[expert-wesley-hoang]] connects [[tool-claude-code]] to [[tool-ai-ark]] via MCP. See [[play-natural-language-icp-list-build]].
- [[expert-patrick-spychalski]] uses [[tool-deepline]] for natural-language sourcing plus [[concept-waterfall-enrichment]] in Claude Code (TAM mapping, account research, competitor reverse-engineering).

## Why it matters

The data tool stops being a destination and becomes an API the agent calls. The GTM engineer's hub becomes the agentic CLI, not the vendor UI. Cheap data (see [[concept-data-commoditisation]]) makes this economical at scale.

## Sources

[[source-wesley-hoang-mcp-lead-lists]], [[source-patrick-spychalski-waterfall-claude-code-deepline]].

## Related

[[concept-waterfall-enrichment]] | [[play-natural-language-icp-list-build]] | [[tool-mcp]] | [[tool-claude-code]] | [[tool-ai-ark]] | [[tool-deepline]]
