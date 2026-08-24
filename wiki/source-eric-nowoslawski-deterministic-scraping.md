---
title: "Source: Eric Nowoslawski -- Crawled thousands of sites for near-nothing with HTML-to-text and keyword matching"
type: source
tags: [source, ai-gtm, enrichment, enrichment-workflow, data, automation]
source-title: "I don't write prompts for list qualification (deterministic scraping at scale)"
source-url: "https://www.linkedin.com/posts/outboundphd_i-dont-write-prompts-for-list-qualification-activity-7465756271334371328-I875"
source-author: Eric Nowoslawski
source-published: unknown
raw-path: raw/Eric Nowoslawski/4.md
last-updated: 2026-06-12
last-updated-time: 23:40
---

# Source: Eric Nowoslawski -- Crawled thousands of sites for near-nothing

> LinkedIn post by [[expert-eric-nowoslawski]]. Raw: `raw/Eric Nowoslawski/4.md`.

## Summary

Eric crawled thousands of websites to score them for ICP fit and paid almost nothing. The method:

- **Free text extraction.** An open-source HTML-to-text converter ([[tool-html2text]]) pulls homepage and footer content fine. Paid tools (ZenRows, Firecrawl) earn their money only on genuinely hard targets: heavy anti-bot, JS-gated content, sites that fight you. "I just want the text on this page" usually is not that.
- **Deterministic scoring, no LLM.** He matched specific compliance keywords in footers. A keyword match does not need a model; bolting one on would be slower, more expensive, and worse.
- **Agent as orchestrator.** [[tool-claude-code]] in goal mode ran it overnight. Ridiculously cheap for thousands of sites.

The general rule that anchors [[concept-deterministic-first]]: every paid API and every AI call in a pipeline should justify why a free, deterministic step could not do it first. Most cannot; they got added because that is the default everyone copies.

## Key takeaways

- Free open-source extraction handles most "just get the text" jobs; reserve paid scrapers for JS-heavy / bot-protected targets (commenters note ~50% of modern sites need a headless fallback).
- Keyword matching beats an LLM for deterministic compliance signals (e.g. "authorised and regulated by the Financial Conduct Authority", "FRN" in a footer).
- The same discipline applies to enrichment: the answer is often in the LinkedIn URL, yet teams pay for a waterfall anyway (commenter Leo Bosuener). Connects to [[concept-waterfall-enrichment]].

## Attribution

[[expert-eric-nowoslawski]], Founder Growth Engine X. LinkedIn post; repo referenced: html2text.
