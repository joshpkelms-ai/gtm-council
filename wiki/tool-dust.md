---
title: "Tool: Dust"
type: tool
tags: [tool, ai-gtm, agentic, automation, tool-integration]
last-updated: 2026-06-13
last-updated-time: 09:00
---

# Tool: Dust

> dust.tt -- a no-code, multiplayer agent-building platform built for teams rather than individuals. Connects to company knowledge across Slack, Google Drive, Notion, GitHub, Salesforce, and Snowflake, and pairs that with the governance controls (permissions, SSO/SCIM, audit logs, role-based access) an org needs to roll agent-building out widely.

## Why it matters here

Dust is the enabling tool behind the Vanta motion in [[source-noah-adelstein-vanta-dust-agent-builders]]. Two layers in one platform make it unusual:

1. **Individual prototyping with shared access.** Anyone with a seat can prototype an agent in an afternoon without opening a terminal, on data sources the GTM Engineering team has gated. The agents they build are available to the rest of the org.
2. **Central oversight.** The GTME team sits on top with admin analytics: who is building what, which agents gain adoption, which workflows are candidates for deeper investment.

That pairing is what makes [[concept-adoption-as-prioritisation]] operable -- reps build, the central team reads the usage signal and productionises the winners (see [[play-adoption-driven-roadmap]]).

## Notes

- Effectiveness depends entirely on the underlying data foundation; Vanta built custom MCPs (see [[tool-mcp]]) on top of [[tool-gong]] and Snowflake to gate access and strip garbage before agents read it. Ties to [[concept-context-assembly]] and [[concept-silent-failures]].
- Positioned against single-player agent tools; the "multiplayer" framing is the differentiator.

## Sources

[[source-noah-adelstein-vanta-dust-agent-builders]] ([[expert-noah-adelstein]], featuring [[expert-shashank-khanna]]).

## Related

[[tool-mcp]] | [[tool-gong]] | [[concept-adoption-as-prioritisation]] | [[play-adoption-driven-roadmap]] | [[concept-context-assembly]]
