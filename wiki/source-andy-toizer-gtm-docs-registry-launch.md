---
title: "Source: Andy Toizer -- Open-sourced a cheat sheet for 184 GTM tools"
type: source
tags: [source, ai-gtm, tool-integration, automation, agentic]
source-title: "Claude Code keeps telling me it can't connect... so I open sourced a cheat sheet for 184 of the top GTM tools"
source-url: https://www.linkedin.com/posts/andy-toizer_claude-code-keeps-telling-me-it-cant-connect-share-7470514810024009728-Gq9H
source-author: Andy Toizer
source-published: unknown
raw-path: raw/Andy Tozier/1.md
last-updated: 2026-06-12
last-updated-time: 23:10
---

# Source: Andy Toizer -- Open-sourced a cheat sheet for 184 GTM tools

> LinkedIn post by [[expert-andy-toizer]]. Raw: `raw/Andy Tozier/1.md`.

## Summary

[[tool-claude-code]] kept saying it "can't connect" to tools that have perfectly good APIs, so Toizer built [[tool-gtm-docs-registry]]. He steals GTM ideas from software engineers, who are ~18 months ahead on coding agents (see [[concept-borrow-from-engineering]]): engineers have Context7 (9,000+ libraries of always-current docs agents pull at runtime), but the GTM stack was not in it. So he built a GTM version in one night.

- 184 GTM tools, each profiled across MCP, API, CLI, OpenAPI, llms.txt, and SDK.
- Every tool scored /5 on agent readiness (62 are 5/5). See [[concept-agent-readiness]].
- Every claim backed by official sources, stamped with a verified date.

Three things he is proud of:
1. **One URL serves both species.** Curl it for JSON; open it in a browser for a human page.
2. **An MCP server about MCP servers.** The agent resolves "hs" to HubSpot and pulls docs without loading the site.
3. **It documents the scary stuff.** Every profile flags destructive operations and exact rate limits (e.g. Instantly's email-list endpoint caps at 20 req/min) before an agent finds out the hard way.

Now instead of "I can't connect to that," he sends Claude Code the link and it figures the rest out. Free and open source: https://gtm-docs-registry.vercel.app/

## Key takeaways

- Agents fail on tools they lack runtime docs for; a retrieval layer fixes it. See [[tool-gtm-docs-registry]].
- Profile every tool for agent readiness across all agent surfaces. See [[concept-agent-readiness]].
- Surface destructive operations and rate limits proactively.

## Attribution

[[expert-andy-toizer]], Head of Growth at Freckle.io, AgentOperator. Original LinkedIn post.
