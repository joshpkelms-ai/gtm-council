---
title: "Play: Cheap list processing (deterministic, then sub-agents, then batch API)"
type: play
tags: [play, ai-gtm, enrichment-workflow, automation, data, agentic]
last-updated: 2026-06-12
last-updated-time: 23:40
---

# Play: Cheap list processing

> Qualify, clean, or score a large list at near-zero incremental cost by tiering the work: free deterministic checks, then coding-agent sub-agents, then the paid batch API only for the remainder. [[expert-eric-nowoslawski]]'s applied version of [[concept-deterministic-first]].

## When to run it

You have thousands to hundreds of thousands of rows that need an ICP pass, a cleanup, or a fit score, and the reflex is to send it all to the batch API.

## The motion

1. **Free deterministic pass.** Extract page text with open-source [[tool-html2text]] (reserve paid scrapers for JS-gated / bot-protected sites). Run keyword/regex matching for deterministic signals (compliance strings, pricing-page presence, etc.). A Python script reads obvious signals; cost $0.
2. **Sub-agent pass for judgment calls.** In [[tool-codex]] or [[tool-claude-code]], prompt "Spawn 10 task sub-agents to handle this for me." A small model (e.g. GPT-5.4-mini / GPT-5 nano) judges fit across the whole list inside your existing subscription; $0 extra and no main-session context-rot. Orchestrate overnight in goal mode (see [[play-agentic-goal-run]]).
3. **Paid batch API for the remainder only.** When the residual volume truly justifies it. On OpenAI, nano/mini cost the same on batch (24h) and flex (10min) tiers, so pick by turnaround.

## Result

Eric cleaned 80,000 rows for $0 extra and crawled thousands of sites for near-nothing. The skill is workflow design: spend expensive intelligence only where judgment is actually required.

## Caveats

Not literally free -- you still pay for data and the coding-agent subscription. There is a crossover where the API is faster overall; above it, pay for the API.

## Sources

[[source-eric-nowoslawski-subagent-list-cleaning]], [[source-eric-nowoslawski-deterministic-scraping]] by [[expert-eric-nowoslawski]].

## Related

[[concept-deterministic-first]] | [[play-agentic-goal-run]] | [[concept-waterfall-enrichment]] | [[tool-html2text]] | [[tool-codex]]
