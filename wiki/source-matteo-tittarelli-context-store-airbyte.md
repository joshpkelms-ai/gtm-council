---
title: "Source: Matteo Tittarelli -- Check what agents read before the skill runs (Context Store)"
type: source
tags: [source, ai-gtm, agentic, data, tool-integration, enrichment]
source-title: "Everyone's too busy running skills. Almost nobody's checking what agents read before the skill even runs."
source-url: "https://www.linkedin.com/posts/matteo-titta_everyones-too-busy-running-skills-almost-activity-7470177855851737088-1igk"
source-author: Matteo Tittarelli
source-published: unknown
raw-path: raw/Matteo Titt/1.md
last-updated: 2026-06-12
last-updated-time: 23:40
---

# Source: Matteo Tittarelli -- Check what agents read before the skill runs

> LinkedIn post by [[expert-matteo-tittarelli]] (Airbyte brand partnership). Raw: `raw/Matteo Titt/1.md`. Anchor source for [[concept-context-assembly]].

## Summary

Everyone is busy running skills; almost nobody checks what the agent reads before the skill even runs. That is where things break. Matteo watched an enrichment agent personalise off a job title that had changed nine months earlier, because the data source and the CRM disagreed on who the contact was, and the agent threw no errors. It had stitched its context together at query time from sources that disagreed with each other. A better prompt does not fix that; the context was already wrong before the model saw it.

The teams getting it right assemble the context first, then let the agent read it. He points to what Mario and team are building at [[tool-airbyte]]: a Context Store that pre-assembles and unifies data so the agent reads one clean view of an account rather than five conflicting ones stitched live; one MCP connection fronting everything across Claude, ChatGPT, and Cursor; and agents that write back to close the loop in the CRM.

## Key takeaways

- The failure is upstream: confidently dumb agent behaviour on good prompts usually means the assembled context was wrong.
- Pre-assemble and unify context into one source of truth before the agent queries it (the "Context Store" pattern).
- One MCP endpoint fronting all context beats many silos with zero shared context.
- Commenter Raouf Lemouchi: stitching records on the fly from conflicting systems is automating bad judgment at scale.

## Attribution

[[expert-matteo-tittarelli]], Genesys Growth. LinkedIn post, Airbyte partnership. "Mario" = Mario Moscatiello (see `raw/Clippings/S2E5 Foundations Before Automation`).
