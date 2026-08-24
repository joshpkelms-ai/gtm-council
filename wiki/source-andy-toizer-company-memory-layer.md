---
title: "Source: Andy Toizer -- I built a company memory layer for GTM agents"
type: source
tags: [source, ai-gtm, agentic, automation, data, messaging]
source-title: "I built a company memory layer for GTM agents"
source-url: "https://agentoperator.substack.com/p/i-built-a-company-memory-layer-for"
source-author: Andy Toizer
source-published: 2026-05-11
raw-path: "raw/Clippings/I built a company memory layer for GTM agents.md"
last-updated: 2026-06-13
last-updated-time: 11:30
---

# Source: Andy Toizer -- I built a company memory layer for GTM agents

> The full AgentOperator writeup of building Freckle's GTM Brain. The longer narrative behind [[framework-gtm-brain]] (the LinkedIn launch is [[source-andy-toizer-gtm-brain]]; this is the build diary). Raw: `raw/Clippings/I built a company memory layer for GTM agents.md`.

## Summary

The blocker was never whether Codex could help with GTM work; it was re-teaching it Freckle every single time (what we do, how pricing works, how we compare to [[tool-clay]], which proof is okay to use). So Toizer built a source-backed **company memory layer** that tells [[tool-codex]], [[tool-claude-code]], and future GTM agents what to trust and where to look.

The lessons that go beyond the launch post:

- **First build failed by being too big.** Asked to build a full ground-up company repo, Codex produced a consulting report: strategy docs, campaign ideas, competitive framing. He did not need the most complete GTM wiki; he needed enough durable context for future agents to do smaller, better work. Forced it into an MVP.
- **Map source-of-truth tools first.** The single most important practical decision. Codex optimised for output and built docs before asking where data lived, so he had it inventory the tool list first. The resulting source map: ChartMogul = revenue truth, [[tool-hubspot]] = CRM truth, PostHog + database = product usage, Gmail/Slack = tone and customer language, Instantly/HeyReach = outbound campaign memory, Fathom/Pylon/shared Slack = pain and proof, Customer.io = lifecycle, Notion = planning, Sybill = call context. The brain does not replace those tools; it tells the agent which tool may answer which question and what still needs human interpretation.
- **Tools provide evidence. Operators provide meaning.** None of those tools can decide what a customer means to positioning; that is the operator's job. The repo's rule: *"Tools provide evidence. Operators provide meaning. The GTM Brain stores the version future agents should use."*
- **Grill Me to capture judgment.** Using the Grill Me skill (Matt Pocock), the agent interrogates the operator rather than accepting its own first plan: ask one pointed question, include the current best hypothesis, explain why it matters and what changes by the answer. Beats approving a long plan in bulk.
- **Language steers the agent.** "If you call something strategy, the agent starts trying to strategise. If you call it context, it does a better job organising and preserving what is already true." He scrubbed "strategy" to "durable context", "working theory", "source-backed evidence", or "accountable-owner review", and added an MVP checklist to stop drift.
- **Refresh without letting agents rewrite truth**, then packaged the whole build as a reusable plugin (the GTM Brain Builder).

## Key takeaways

- The brain is a routing-and-judgment layer, not a data dump: which source answers which question, and where a human must make the meaning call.
- Map source-of-truth tools before writing any context.
- Separate evidence (tools) from meaning (operators); store the operator-approved version for agents.
- Mind the words: "context" makes the agent preserve truth; "strategy" makes it improvise.

## Attribution

[[expert-andy-toizer]], Head of Growth at Freckle.io, AgentOperator. Companion launch post: [[source-andy-toizer-gtm-brain]]. Framework: [[framework-gtm-brain]].
