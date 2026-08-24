---
title: "Concept: Agent readiness (can an agent operate this tool?)"
type: concept
tags: [concept, ai-gtm, tool-integration, agentic, automation]
last-updated: 2026-06-12
last-updated-time: 23:10
---

# Concept: Agent readiness

> A measure of how directly an AI agent can operate a tool, based on its available agent surfaces (MCP, API, CLI, OpenAPI/spec, llms.txt, SDK) and the quality of its docs. Not a measure of product quality.

## The idea

[[expert-andy-toizer]] profiles GTM tools for agent readiness in [[tool-gtm-docs-registry]], scoring each /5:

- **5** -- strong official agent surface: API, specs, SDKs, or clear operational docs.
- **4** -- good official API/docs with minor gaps.
- **3** -- usable but requires interpretation or source stitching.
- **2** -- weak official support; community or wrapper evidence may be needed.
- **1** -- minimal agent-operable surface.

Of 184 published GTM tools, 62 score 5/5. Scores describe documentation and interface readiness, not product rankings.

## Why it matters

Agents fail on tools they lack runtime docs for ("I can't connect to that"), even when the tool has a perfectly good API. Knowing a tool's agent surfaces, and the scary bits (destructive operations, exact rate limits like Instantly's 20 req/min email-list cap), is what lets an agent operate it safely. Agent readiness is the practical gate on [[concept-agentic-sourcing]] and any agent-driven workflow.

## Design for it, not just measure it

Agent readiness applies to artefacts you build, not only tools you buy. [[expert-rafid-imran]] rebuilt a marketing site so that "every tech in the stack is something Claude Code can understand" -- schemas, file conventions, validators, and skills readable to an agent the same way they are to a human -- which is what let one person operate the whole site through an agent. Building for agent-readiness is the upstream choice behind [[play-code-first-marketing-site]].

## Sources

[[source-andy-toizer-gtm-docs-registry-launch]], [[source-andy-toizer-gtm-docs-registry-readme]].

## Related

[[tool-gtm-docs-registry]] | [[tool-mcp]] | [[concept-agentic-sourcing]] | [[concept-borrow-from-engineering]] | [[play-code-first-marketing-site]] | [[expert-andy-toizer]]
