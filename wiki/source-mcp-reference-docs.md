---
title: "Source: MCP reference docs (protocol, server tutorial, Apify connectors)"
type: source
tags: [source, reference, tool-integration, agentic, ai-gtm, automation]
source-title: "Model Context Protocol (GitHub) | Build an MCP server | Announcing MCP connectors"
source-url: "https://github.com/modelcontextprotocol | https://modelcontextprotocol.io/docs/develop/build-server | https://blog.apify.com/announcing-mcp-connectors/"
source-author: "Model Context Protocol project; Apify (Jan Curn)"
source-published: "2026-06-09 (Apify); others undated"
raw-path: "raw/Clippings/Model Context Protocol.md, raw/Clippings/Build an MCP server.md, raw/Clippings/Announcing MCP connectors.md"
last-updated: 2026-06-13
last-updated-time: 10:30
---

# Source: MCP reference docs (protocol, server tutorial, Apify connectors)

> Three reference clippings on the Model Context Protocol, distilled into [[tool-mcp]]. Ingested as one body. Raw: `raw/Clippings/`.

## What this is

- **Model Context Protocol (GitHub readme)** -- MCP is an open protocol for seamless integration between LLM applications and external data sources and tools, with official SDKs across TypeScript, Python, Java, Kotlin, C#, Go, PHP, Ruby, Rust, and Swift.
- **Build an MCP server (modelcontextprotocol.io tutorial)** -- the hands-on quickstart. A server can expose three capability types: **resources** (file-like readable data), **tools** (functions the LLM can call, with user approval), and **prompts** (pre-written templates). The tutorial builds a weather server exposing two tools and connects it to a host.
- **Announcing MCP connectors (Apify)** -- a product instance: Apify Actors can now securely reach third-party apps (Notion, GitHub, Slack, Postgres, Google Calendar) through MCP, so a scraping workflow can act on the outer world under an authenticated account rather than only collecting anonymous public data.

## Why it matters here

These are the protocol-level foundation under [[tool-mcp]]'s role in the corpus: the wire that turns data vendors and workflow platforms into things an agent can call from a conversation ([[concept-agentic-sourcing]]). The resources / tools / prompts split is the mental model practitioners reach for; the Apify connectors release shows the ecosystem maturing from "read the public web" to "act under an account", which is the same authenticated-write caution [[expert-patrick-spychalski]] applies to CRM writes ([[play-agentic-prospect-clay-crm-push]]).

## Key takeaways

- MCP exposes three capability types: resources, tools, prompts. Tools dominate current use.
- It is a protocol, so any client can call any server; reusability is the point.
- Connectors extend agents from reading public data to acting on authenticated apps.

## Attribution

Model Context Protocol project (modelcontextprotocol.io / GitHub); Apify connectors post by Jan Curn. See [[tool-mcp]]. Companion GTM-specific workshop: [[source-cargo-mcp-gtm-workshop]].
