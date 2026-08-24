---
title: "Source: Patrick Spychalski -- Waterfall enrichment in Claude Code has arrived (Deepline)"
type: source
tags: [source, ai-gtm, enrichment, agentic, enrichment-workflow]
source-title: "Waterfall enrichment in Claude Code has arrived"
source-url: https://www.linkedin.com/posts/patrickspychalski_waterfall-enrichment-in-claude-code-has-arrived-activity-7465391361685483521-n61D
source-author: Patrick Spychalski
source-published: unknown
raw-path: raw/Patrick Spychalski/1.md
last-updated: 2026-06-12
last-updated-time: 22:30
---

# Source: Patrick Spychalski -- Waterfall enrichment in Claude Code has arrived (Deepline)

> LinkedIn post plus video transcript by [[expert-patrick-spychalski]]. Raw: `raw/Patrick Spychalski/1.md`.

## Summary

[[tool-deepline]] brings [[concept-waterfall-enrichment]] into [[tool-claude-code]]. The concept: prompt Claude in natural language to source a list of companies or people; Deepline assembles it. Then enrich for basic data points (phone numbers, emails) across several providers. More interesting, it uses tools like [[tool-exa]] to run agentic research tasks and write the results to the table. View results in a table by session id (easy to export), or use native Snowflake / Salesforce / HubSpot connections to write there directly.

The video frames Deepline as Clay's data-provider waterfall ported to a CLI: [[tool-clay]] invented the waterfall, Deepline translates it into Claude Code. Deepline's bet is that GTMs will use Claude Code (or an equivalent agentic CLI) as their main hub, so they should have an API that does sourcing, enrichment, and delivery. Credit-based pricing like Clay's; every action shows the source and cost. Demo: "find me five CTOs at New York-based startups," then "add phone numbers and how long they've been in their job" -- done seamlessly, viewable in a session table.

Comments add real-world colour: used heavily for TAM mapping (Deepline ships a `/build-tam` skill and a free company search database), account research, reverse-engineering competitors, and testing what data providers (e.g. Crustdata) offer. One user layers a B2B-signals MCP on top: pull hiring and competitor-engagement signals first, then run the waterfall only on companies that pass the filter, saving ~60% of enrichment credits.

## Key takeaways

- Waterfall enrichment is no longer Clay-only; it runs in an agentic CLI. See [[concept-waterfall-enrichment]].
- Agentic sourcing from natural language plus agentic research (Exa) plus direct CRM/warehouse writes. See [[concept-agentic-sourcing]].
- Filter on signals before enriching to cut credit spend.

## Attribution

[[expert-patrick-spychalski]], Co-Founder at The Kiln. Original LinkedIn post and video walkthrough. Deepline co-founder Jai Toor appears in comments.
