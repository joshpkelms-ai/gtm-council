---
title: "Concept: Context assembly (assemble before the agent reads)"
type: concept
tags: [concept, ai-gtm, agentic, data, tool-integration, enrichment]
last-updated: 2026-06-13
last-updated-time: 11:30
---

# Concept: Context assembly

> Assemble and unify an agent's context upstream, into one clean view, before the agent reads it. If context is stitched together at query time from sources that disagree, no prompt can save it; you are automating bad judgment at scale. [[expert-matteo-tittarelli]]'s framing of the upstream-context problem. [[expert-jacob-dietle]] gives the canonical definition: context is "information that changes the meaning of other information", and AI amplifies whatever you give it.

## The failure mode

Teams obsess over the skill and ignore what the agent reads before the skill runs. An enrichment agent personalised off a job title that had changed nine months earlier, because the data source and CRM disagreed on who the contact was, and it threw no errors. The context was wrong before the model saw it. Confidently dumb behaviour on good prompts is the tell that the problem is upstream.

## The pattern

Pre-assemble and unify data into one source of truth, then let the agent read that single clean view of an account, not five conflicting ones stitched live. Front it with one MCP endpoint that follows the agent across Claude, ChatGPT, and Cursor, and let agents write back to close the loop in the CRM. In the corpus this is the "Context Store" pattern from [[tool-airbyte]].

## The context OS, and build vs buy

[[expert-jacob-dietle]] frames the whole effort as building a **context OS** and treats "context ops" as a new function, the GTM analogue of DevOps, owned by a subject-matter "benevolent dictator". Practical discipline:

- **Foundation before scope.** Build a small house on a strong foundation; find the context bottleneck (give it transcripts but no ICP and it hallucinates). Pick three starting use cases.
- **Iterate via back-pressure.** Decompose a known-good example into testable building blocks (tone, sources, structure) and feed the missing context each round, moving output from ~60% to ~85%. The GTM substitute for software's unit tests.
- **Solve once, compound.** Turn a solved process into a skill so the team inherits it; the same context feeds content, signals, outbound, and ads ("relevant beats personalised").
- **Build and buy.** Build your own deep workspace ([[tool-claude-code]] / Codex) for customisation, control of how context flows, and understanding; buy an opinionated tool like [[tool-octave]] for multiplayer mode and non-technical reps. Do both. See [[source-jacob-dietle-context-engineering]].

The "tools provide evidence, operators provide meaning" rule from [[framework-gtm-brain]] is the same idea at the governance layer: the data layer resolves facts, the human supplies interpretation.

## Relation to the brain repos

This is the upstream-assembly sibling of the context-repo frameworks: [[framework-gtm-brain]] (Toizer) routes every fact to its owning source before promoting it to "company truth"; [[framework-ai-employee-loop]] (Nowoslawski) builds a company brain and refreshes it on a schedule. Context-assembly stresses unifying conflicting sources at the data layer rather than the prompt layer. It also pairs with [[concept-claim-tagging]]: resolve and source the data before it reaches the model.

## Source

[[source-matteo-tittarelli-context-store-airbyte]] by [[expert-matteo-tittarelli]]; [[source-jacob-dietle-context-engineering]] by [[expert-jacob-dietle]].

## Related

[[tool-airbyte]] | [[tool-octave]] | [[framework-gtm-brain]] | [[framework-ai-employee-loop]] | [[concept-claim-tagging]] | [[concept-foundations-before-automation]] | [[expert-jacob-dietle]] | [[tool-mcp]]
