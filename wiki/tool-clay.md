---
title: "Tool: Clay"
type: tool
tags: [tool, enrichment, automation, tool-integration, enrichment-workflow]
last-updated: 2026-06-13
last-updated-time: 13:00
---

# Tool: Clay

> The category-defining GTM data and enrichment platform. Invented the data-provider waterfall. Now exposes built workflows to LLMs via an MCP.

## What it is

A spreadsheet-style platform for sourcing, enriching, qualifying, and routing GTM data, with a large library of integrated data providers. Clay invented the [[concept-waterfall-enrichment]]: query providers in priority order until a field is filled, paying per hit.

## Position in the corpus

- **Reference point for the agentic turn.** [[tool-deepline]] is repeatedly framed as "Clay's waterfall ported to a CLI" ([[tool-claude-code]]). See [[source-patrick-spychalski-waterfall-claude-code-deepline]].
- **Clay MCP.** Clay launched a rep-facing [[tool-mcp]]: not for building tables in Claude Code, but for calling built Clay functions from an LLM (OpenAI or Claude). Clay's stance is that reps should not use the platform directly; workflows should be fronted by something friendlier. See [[source-patrick-spychalski-clay-mcp]] and [[play-agentic-prospect-clay-crm-push]].
- **Trusted write layer.** A rule-aware Clay function is trusted for CRM / sequencer / warehouse writes where a raw agent is not.
- **The data layer in the data-vs-reasoning split.** As the Clay-to-Claude-Code debate matured, the settled frame is that Clay supplies breadth and accuracy (the data layer) while Claude supplies depth and judgment (the reasoning layer) -- and Clay's own AI column already runs Claude. See [[concept-data-vs-reasoning-layer]] ([[expert-sachin-jha]], [[expert-garrett-wolfe]]). [[expert-patrick-schaber]] shows the non-engineer path: Clay rendered inside Claude Cowork, scored against a stored ICP. Its limits (the ~100-column ceiling, logic trapped in the table) are exactly what pushes reasoning out of Clay.
- **Built by agents, two ways.** [[expert-eric-nowoslawski]] (a Clay Enterprise Partner) builds Clay tables with agents via [[tool-browser-use]] reading Clay's front-end API, and via a new Clay CLI in [[play-agentic-goal-run]]; his open-source `autoclay` skill scaffolds tables. Clay has no public API, so the browser/CLI is the integration surface.

## Functions

Clay's Functions feature (2026, on all paid plans) lets you package a workflow once and call it from any table: define inputs and outputs, save, and every caller gets one clean column while the logic runs in a hidden background table. Unlike templates (copy-paste, which drift), a function is **called not copied**, so editing it propagates everywhere automatically. This is the single-source-of-truth principle [[concept-gtm-functions]], and the natural home for a [[concept-waterfall-enrichment]]. Functions support governance (conditional/compliance gating), a credit-cost catalogue, unlimited rows via pass-through, and -- critically -- are callable from outside Clay (Claude, ChatGPT, Glean) over [[tool-mcp]]. See the full course [[source-clay-functions-course]] and the build motion [[play-clay-function-library]].

## Sculptor

Sculptor is Clay's conversational AI copilot for analysing GTM data in plain English: it understands full GTM-workflow context and answers questions over connected data (Salesforce accounts enriched with Mixpanel usage, Snowflake lists, inbound leads with buying signals) with no SQL and no waiting on a data team. Flagship workflow: derive a real ICP from closed-won and active customers (breakdowns by size, revenue, deal size, credits, champion personas) and get recommended Clay search filters to find lookalikes. This is Clay reaching up into the reasoning/analysis layer on top of its own data layer, an in-product instance of [[concept-data-vs-reasoning-layer]]. See [[source-clay-sculptor]].

## Pricing

Usage-based / credit pricing; Deepline mirrors this model.

## Related

[[tool-deepline]] | [[tool-mcp]] | [[concept-waterfall-enrichment]] | [[concept-data-vs-reasoning-layer]] | [[concept-gtm-functions]] | [[play-agentic-prospect-clay-crm-push]] | [[tool-browser-use]] | [[source-clay-sculptor]] | [[expert-patrick-spychalski]] | [[expert-jared-waxman]] | [[expert-eric-nowoslawski]] | [[expert-garrett-wolfe]] | [[expert-patrick-schaber]]
