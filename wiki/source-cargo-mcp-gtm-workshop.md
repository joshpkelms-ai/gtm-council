---
title: "Source: Cargo workshop -- Build and run your MCP Server for GTM (Joe Rhew)"
type: source
tags: [source, ai-gtm, tool-integration, agentic, automation, outbound]
source-title: "Build and run your MCP Server for GTM"
source-url: "https://www.youtube.com/watch?v=lpi9SDd9j94"
source-author: "Cargo (host); Joe Rhew (guest, The Workflow Company)"
source-published: 2025-05-30
raw-path: "raw/Clippings/Build and run your MCP Server for GTM.md"
last-updated: 2026-06-13
last-updated-time: 10:30
---

# Source: Cargo workshop -- Build and run your MCP Server for GTM (Joe Rhew)

> A Cargo-hosted workshop with Joe Rhew on standing up a GTM-specific MCP server. Raw: `raw/Clippings/Build and run your MCP Server for GTM.md`.

## Summary

A hands-on workshop framing [[tool-mcp]] for go-to-market, then showing how to build a custom GTM MCP server without writing code via [[tool-cargo]]. Joe Rhew (founder/CEO of The Workflow Company, an AI-native GTM automation consultancy) walks through the why and the how; Cargo's host runs the no-code build.

Core argument:

- **MCP as a context shortcut.** Instead of pasting a prospect's title, company, and history into Claude by hand, MCP brings that context in on demand: "Claude, fetch this person's recent LinkedIn posts and find an angle." The main current use case is an **API gateway** between LLM clients and the tools you want to call.
- **Resources, prompts, tools.** A server can offer three things: resources (data pushed to the client, e.g. a prospect's experience as JSON), prompts (context-aware templates with dynamic variables, underexplored today), and tools (abstracted functions, e.g. find an email, send via a Gmail MCP). Tools are the dominant use case.
- **Why custom servers.** Few public GTM tools are MCP-ready, so Rhew coded custom TypeScript tools (pull a LinkedIn URL, read the profile, surface the interesting angle) and hosted them remotely. Cargo's pitch: GTM engineers should not spend time on TypeScript and hosting; spin a server up no-code, prototype, ship, and custom-code later if needed.
- **Why it is a big deal vs custom GPTs.** It is a *protocol*: set up one server and any client can call it, and you can expose it to anyone. Old custom tool-calling code was locked to one person's use case and demanded glue infrastructure.
- **When to use it (and not).** Much current MCP value is prototyping and shaping workflows with LLMs; do not reflexively rip out existing API layers to replace them with MCP. Everything is a trade-off: custom code gives full control, no-code gives speed to ship.
- **Closing advice.** The space moves fast; carve out 10-20% of weekly time to tinker with no business objective, just to keep up.

## Key takeaways

- MCP's GTM role today is an API gateway that pulls prospect context and runs tools (research, find email, send) from a chat client.
- Three server capabilities: resources, prompts, tools; tools dominate.
- A protocol beats bespoke tool-calling because any client can reuse any server.
- No-code MCP server building (Cargo) lowers the barrier; custom-code only when you need control.

## Attribution

Joe Rhew, founder/CEO of The Workflow Company, in a workshop hosted by [[tool-cargo]] for its GTM engineer community. Companion protocol references: [[source-mcp-reference-docs]]. See [[tool-mcp]].
