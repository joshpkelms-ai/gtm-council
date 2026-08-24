---
title: "Concept: AEO (answer engine optimisation)"
type: concept
tags: [concept, ai-gtm, content, messaging, reporting]
last-updated: 2026-06-12
last-updated-time: 12:05
---

# Concept: AEO (answer engine optimisation)

> Structuring web content so large language models can parse and cite it, the way SEO targets search rankings. As buyers ask ChatGPT, Claude, Perplexity, and Gemini before Google, getting cited by the answer engine becomes a pipeline channel. [[expert-matteo-tittarelli]]'s framing.

## Why it matters

More buyers consult AI assistants before (or instead of) Google. That traffic is invisible in standard analytics: no bounce rate to fix, no keyword to chase, just a slow leak of pipeline to whoever the AI cited this week. Most sites read well to humans but look unstructured to an LLM (sloppy HTML, missing metadata, slow pages, no schema), so they do not get cited. Almost nobody optimises for citations yet, so the gap is wide but closing fast.

## What "AEO-ready" looks like

Clean HTML, fast load times, structured metadata, schema, sound header hierarchy, and auto-updating sitemaps, so an LLM can actually read and quote the page. Example scoring dimensions (from Framer's AEO Scanner): Findable, Quotable, Understandable, Trustworthy. Common gaps: missing schema, broken header hierarchy, missing internal links, content the AI cannot parse.

## The build, in practice

[[expert-rafid-imran]] shows what AEO-ready looks like when baked into a code-first site rather than bolted on: a markdown serving layer at /llms.txt and .md endpoints so ChatGPT, Perplexity, Claude, and AI Overviews read and cite pages cleanly; JSON-LD structured data on every page; and server-rendered HTML by default so crawlers see real content, not a loading state. Codified as a Claude Code skill that runs on every page before it ships. See [[source-rafid-imran-code-first-marketing-site]] and [[play-code-first-marketing-site]].

## Field signal

The GTM Engineer Pulse tracks the trend: Google published its first official AEO guide; Buffer reported ChatGPT-referred signups up 70% week on week; the prevailing view is that SEO remains the foundation for AI search. See [[source-matteo-tittarelli-gtm-engineer-pulse]].

## Sources

[[source-matteo-tittarelli-aeo-framer-scanner]], [[source-matteo-tittarelli-gtm-engineer-pulse]] by [[expert-matteo-tittarelli]]; [[source-rafid-imran-code-first-marketing-site]] by [[expert-rafid-imran]] (the build).

## The demand-side counterpart

AEO is the mechanics of getting cited; [[concept-ai-first-buyer-journey]] ([[expert-alon-even]]) is the demand-side reason it matters, and the warning that citation mechanics without real peer / dark-social signal behind them are hollow.

## Related

[[tool-framer]] | [[concept-context-assembly]] | [[concept-ai-first-buyer-journey]] | [[expert-alon-even]] | [[expert-matteo-tittarelli]]
