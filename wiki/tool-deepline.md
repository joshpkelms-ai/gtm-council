---
title: "Tool: Deepline"
type: tool
tags: [tool, enrichment, agentic, ai-gtm, enrichment-workflow]
last-updated: 2026-06-12
last-updated-time: 22:30
---

# Tool: Deepline

> GTM-engineering APIs for [[tool-claude-code]]. Ports [[tool-clay]]'s data-provider waterfall into an agentic CLI: source in natural language, enrich across providers, run agentic research, and write to the warehouse or CRM.

## What it is

A sourcing-and-enrichment plugin / API for Claude Code (tagline: "GTM Engineering APIs for Claude Code"). Co-founded by Jai Toor (ex-Uber, Capchase, Datafold) and Chirag Toprani.

## What it does

- **Source in natural language.** Prompt for a list of companies or people; Deepline assembles it. Demo: "find me five CTOs at New York-based startups."
- **Waterfall enrichment.** Enrich for emails, phones, and more across multiple providers (e.g. Crustdata). See [[concept-waterfall-enrichment]].
- **Agentic research.** Uses tools like [[tool-exa]] to run research tasks and write results to the table (e.g. tenure in role).
- **View and route.** View results in a table by session id (easy export), or write to Snowflake / Salesforce / HubSpot via native connections.
- **Skills.** Ships a `/build-tam` skill and a free company-search database; common uses are TAM mapping, account research, and reverse-engineering a company's competitors.

## Pricing

Credit-based, like [[tool-clay]]; every action reports its source and cost.

## Notes

Layer a signals MCP on top and run the waterfall only on companies that pass a hiring/competitor-engagement filter to cut enrichment credits (~60% saved in one report).

## Sources

[[source-patrick-spychalski-waterfall-claude-code-deepline]].

## Related

[[tool-clay]] | [[tool-claude-code]] | [[tool-exa]] | [[concept-waterfall-enrichment]] | [[concept-agentic-sourcing]] | [[expert-patrick-spychalski]]
