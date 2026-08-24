---
title: "Source: Andy Toizer -- GTM Docs Registry (technical README)"
type: source
tags: [source, ai-gtm, tool-integration, automation, agentic]
source-title: "GTM Docs Registry -- source-backed documentation retrieval for GTM tools"
source-url: https://github.com/Andytoizer/gtm-docs-registry
source-author: Andy Toizer
source-published: unknown
raw-path: raw/Andy Tozier/GTM Docs Registry.md
last-updated: 2026-06-12
last-updated-time: 23:10
---

# Source: Andy Toizer -- GTM Docs Registry (technical README)

> Project README by [[expert-andy-toizer]]. Raw: `raw/Andy Tozier/GTM Docs Registry.md`. See also the tool page [[tool-gtm-docs-registry]].

## Summary

The technical design of [[tool-gtm-docs-registry]]: source-backed documentation retrieval that lets agents resolve a GTM product by name and fetch operational docs, then decide how to use it via official MCP, CLI, API, OpenAPI/spec, llms.txt, SDK, or community interfaces. It is for agent builders and coding agents, not a buying guide, ranking site, or recipe library. The agent composes the workflow; the registry supplies retrieval.

- **Scale:** 196 profiles in the repo, 184 published in the hosted catalog.
- **Agent flow:** `resolve-tool-id("hubspot")` then `get-tool-docs("/gtm/hubspot", topic="contacts API auth")`.
- **Data model:** per tool, `tool.json` (metadata, aliases, `agentReadinessScore`, `lastVerified`, interface availability), `docs.md` (agent-facing: auth, key objects/actions, pagination, rate limits, webhooks, destructive ops, caveats), optional `reference.md` (dense endpoint/schema tables), `sources.json` (source URLs + verification). `registry.json` indexes all tools.
- **Surfaces:** local CLI, MCP stdio server (`resolve-tool-id`, `get-tool-docs`, `get-tool-sources`, `search-tools` plus `gtm://` resources), and a read-only HTTP server with `/llms.txt`, `/llms-full.txt`, `/openapi.json`, `/mcp`. Same docs route serves human HTML or agent JSON by request type or `?format=`.
- **Status values:** published / needs-review / draft / monitoring. `agentReadinessScore` is 1-5 for how directly an agent can operate the tool (5 = strong official agent surface). Scores are not product rankings.
- **Freshness:** profiles refreshed when a tool changes its agent surfaces, auth, rate limits, or object model; `lastVerified` dates recorded; stale-but-valid profiles stay available with honest caveats.
- **Research order:** official MCP, CLI, API, OpenAPI, llms.txt, SDK/GitHub, then strong community, then wrappers (Zapier/Make/Pipedream). Prefer official; do not invent capabilities; mark unclear profiles `needs-review` with the exact question.
- **Non-goals:** no recipes, no marketplace, no rankings, no unsupported claims.

## Key takeaways

- A retrieval layer, not a blog post: source-backed, versioned, honestly caveated.
- Agent-readiness scoring describes documentation/interface readiness, not product quality. See [[concept-agent-readiness]].
- Provenance discipline mirrors [[concept-claim-tagging]]: prefer official sources, mark unofficial, never fabricate.

## Attribution

[[expert-andy-toizer]]. GitHub README (github.com/Andytoizer/gtm-docs-registry). Hosted: gtm-docs-registry.vercel.app.
