---
title: "Concept: Waterfall enrichment"
type: concept
tags: [concept, enrichment, enrichment-workflow, data, ai-gtm]
last-updated: 2026-06-12
last-updated-time: 22:30
---

# Concept: Waterfall enrichment

> Query a sequence of data providers in priority order until a data point (email, phone, firmographic) is found, paying per successful hit. Pioneered in [[tool-clay]]; now ported into agentic CLIs.

## The mechanic

Rather than relying on one provider, a waterfall hits provider A, then B, then C, until the requested field is filled, reporting the source and cost of each call. This maximises coverage and accuracy while controlling spend. [[tool-clay]] invented the data-provider waterfall.

## The agentic turn

[[tool-deepline]] translates the waterfall into [[tool-claude-code]]: prompt in natural language to source a list, enrich it across providers (e.g. Crustdata), run agentic research with [[tool-exa]], and write results to a session table or straight to Snowflake / Salesforce / HubSpot. See [[source-patrick-spychalski-waterfall-claude-code-deepline]].

## Spend discipline

Filter before you enrich. One practitioner layers a B2B-signals MCP on top: pull hiring and competitor-engagement signals first, then run the waterfall only on companies that pass the filter, saving ~60% of enrichment credits. Connects to [[concept-agentic-sourcing]].

## Sources

[[source-patrick-spychalski-waterfall-claude-code-deepline]] by [[expert-patrick-spychalski]].

## Related

[[tool-clay]] | [[tool-deepline]] | [[tool-exa]] | [[concept-agentic-sourcing]] | [[concept-data-commoditisation]]
