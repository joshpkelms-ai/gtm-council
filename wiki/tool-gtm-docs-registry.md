---
title: "Tool: GTM Docs Registry"
type: tool
tags: [tool, ai-gtm, tool-integration, agentic, automation]
last-updated: 2026-06-13
last-updated-time: 10:30
---

# Tool: GTM Docs Registry

> Source-backed documentation retrieval for GTM tools, built by [[expert-andy-toizer]]. The GTM analogue of Context7: an agent resolves a tool by name and pulls current, source-stamped operational docs at runtime. Free and open source.

## What it is

A retrieval layer (not a buying guide, ranking site, or recipe library) that lets agents resolve a GTM product by name and fetch operational docs, then decide how to operate it via its MCP, CLI, API, OpenAPI/spec, llms.txt, SDK, or community interfaces. The agent composes the workflow; the registry supplies retrieval.

- 196 profiles in the repo; 184 published in the hosted catalog. 62 score 5/5 on [[concept-agent-readiness]].
- Each tool profiled across MCP, API, CLI, OpenAPI, llms.txt, and SDK, with every claim source-backed and `lastVerified`-stamped.
- Flags destructive operations and exact rate limits per tool.

## How agents use it

`resolve-tool-id("hubspot")` then `get-tool-docs("/gtm/hubspot", topic="contacts API auth")`. It is "an MCP server about MCP servers": the agent resolves "hs" to HubSpot and pulls docs without loading the site.

## Surfaces

- **CLI:** `list`, `resolve`, `docs`, `sources`, `search`.
- **MCP stdio server:** `resolve-tool-id`, `get-tool-docs`, `get-tool-sources`, `search-tools`, plus `gtm://` resources.
- **HTTP server / hosted API** (gtm-docs-registry.vercel.app): `/catalog`, `/registry`, `/llms.txt`, `/llms-full.txt`, `/openapi.json`, `/mcp`. The same URL serves human HTML or agent JSON depending on the request (or `?format=`).

## Data model and discipline

Per tool: `tool.json` (metadata, aliases, `agentReadinessScore`, `lastVerified`, interfaces), `docs.md` (auth, objects, actions, pagination, rate limits, webhooks, destructive ops, caveats), optional `reference.md` (dense endpoint/schema tables), `sources.json`. Status: published / needs-review / draft / monitoring. Research prefers official sources over community over wrappers; unclear profiles are marked `needs-review` with the exact open question. Non-goals: no recipes, rankings, or unsupported claims.

## Sources

[[source-andy-toizer-gtm-docs-registry-launch]], [[source-andy-toizer-gtm-docs-registry-readme]]. GitHub: github.com/Andytoizer/gtm-docs-registry. Two further Clippings copies (the GitHub readme and the live site landing page at gtm-docs-registry.vercel.app) are the same product on different surfaces and add nothing beyond the above; folded here rather than given their own source pages.

## Related

[[concept-agent-readiness]] | [[concept-borrow-from-engineering]] | [[tool-mcp]] | [[expert-andy-toizer]]
