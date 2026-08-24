---
title: "Play: Agentically prospect, then push through Clay to the CRM"
type: play
tags: [play, agentic, ai-gtm, tool-integration, enrichment-workflow]
last-updated: 2026-06-12
last-updated-time: 22:30
---

# Play: Agentically prospect, then push through Clay to the CRM

> Use an agent for the open-ended prospecting, but route system-of-record writes through a pre-built [[tool-clay]] function that enriches, normalises, and knows your rules. Best of both worlds: agentic discovery, governed write.

## The problem it solves

GTM engineers want agentic speed but do not yet trust a raw agent to operate inside the CRM, sequencer, or data warehouse. A deterministic, rule-aware Clay table is trustworthy for the write; the agent is trustworthy for the search.

## Steps

1. **Prospect agentically.** Build and enrich the list in an agentic CLI (see [[play-natural-language-icp-list-build]], [[concept-agentic-sourcing]]).
2. **Build a Clay function** for the specific write task: enrich, qualify, normalise, push to CRM / sequencer / warehouse.
3. **Expose the function to Clay's [[tool-mcp]]** (rep-facing; currently callable from OpenAI or Claude).
4. **Call it from the command line** to push the prospected list through the governed table.

## Why split it this way

The agent handles ambiguity and breadth; the Clay table enforces system rules and data hygiene on the way into the system of record. Avoids letting an agent "play around" in the CRM directly.

## Source

[[source-patrick-spychalski-clay-mcp]] by [[expert-patrick-spychalski]].

## Related

[[tool-clay]] | [[tool-mcp]] | [[concept-agentic-sourcing]] | [[play-natural-language-icp-list-build]]
