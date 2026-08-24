---
title: "Source: Eric Nowoslawski -- Cleaning 80k rows with coding-agent sub-agents, not the batch API"
type: source
tags: [source, ai-gtm, agentic, enrichment-workflow, data, automation]
source-title: "The biggest cost hack in list building right now (sub-agents to clean lists)"
source-url: "https://www.linkedin.com/posts/outboundphd_the-biggest-cost-hack-in-list-building-right-activity-7463574704591728640-CU1e"
source-author: Eric Nowoslawski
source-published: unknown
raw-path: raw/Eric Nowoslawski/6.md
last-updated: 2026-06-12
last-updated-time: 23:40
---

# Source: Eric Nowoslawski -- Cleaning 80k rows with coding-agent sub-agents

> LinkedIn post by [[expert-eric-nowoslawski]]. Raw: `raw/Eric Nowoslawski/6.md`.

## Summary

The cost hack: ask [[tool-codex]] or [[tool-claude-code]] to use sub-agents to clean lists instead of paying for batch-API tokens. He had 80,000 rows needing an ICP pass; rather than send them to the batch API, he told Codex to spin up a task sub-agent to judge fit. It ran a GPT-5.4-mini sub-agent across all 80,000, sorting good from bad, on his $200 Codex plan with no extra API cost. He still has ~40% of weekly usage left most weeks; the allowance is hard to spend.

The order of operations (the backbone of [[concept-deterministic-first]] and [[play-cheap-list-processing]]):

1. **Free deterministic checks first** -- a Python script reading obvious page signals: $0.
2. **Coding-agent task sub-agents for judgment calls** -- included in usage you already pay for: $0 extra.
3. **Paid batch API only for the remainder**, when volume truly justifies it.

To trigger it in-session without being pushed to the API, ask: "Spawn 10 task sub-agents to handle this for me." There is a crossover point where the API is faster overall; for those cases, GPT-5 nano and mini cost the same on batch (24h) and flex (10min) tiers.

## Key takeaways

- Sub-agents are effectively free judgment-call labour inside an existing coding-agent subscription.
- They also avoid context-rot in the main session, giving better results (commenter Yusuf Ahmed).
- It is not literally zero: you still pay for data and the subscription (commenter Cezar Halmagean); the saving is on incremental API spend.

## Attribution

[[expert-eric-nowoslawski]], Founder Growth Engine X. LinkedIn post.
