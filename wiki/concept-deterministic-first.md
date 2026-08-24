---
title: "Concept: Deterministic-first (make every paid API and AI call justify itself)"
type: concept
tags: [concept, ai-gtm, enrichment-workflow, automation, data]
last-updated: 2026-06-12
last-updated-time: 23:40
---

# Concept: Deterministic-first

> [[expert-eric-nowoslawski]]'s spend discipline for GTM pipelines: every paid API and every AI call must justify why a free, deterministic step could not do it first. Most cannot; they got added because that is the default everyone copies.

## The order of operations

1. **Free deterministic checks first.** A Python script reading obvious signals off a page; open-source HTML-to-text extraction ([[tool-html2text]]); keyword/regex matching. Cost: $0. A keyword match (e.g. an FCA-regulation footer string) does not need an LLM, and bolting one on is slower, costlier, and worse.
2. **Coding-agent sub-agents for judgment calls.** Spin up task sub-agents inside an existing [[tool-codex]] / [[tool-claude-code]] subscription. Included in usage you already pay for; effectively $0 extra. Also avoids main-session context-rot.
3. **Paid batch API only for the remainder**, when volume genuinely justifies it. (On OpenAI, GPT-5 nano/mini cost the same on batch and flex tiers.)

Worked example: 80,000 rows given an ICP pass for no incremental cost (deterministic script + GPT-5.4-mini sub-agent), with the batch API reserved for what was left.

## Where it bites

- **Scraping.** Open-source text extraction handles most "just get the text" jobs; reserve paid scrapers (ZenRows, Firecrawl) for JS-gated / bot-protected targets.
- **Scoring.** Use deterministic matching for deterministic signals; reserve the model for genuine judgment.
- **Enrichment.** The answer is often already in the LinkedIn URL; do not pay for a waterfall when a cheap step would do. Sharpens [[concept-waterfall-enrichment]]'s "filter before you enrich".

## Independently restated

[[expert-garrett-wolfe]] arrives at the same rule from the Claude Code side and calls it "code-first, not AI-first": title/school/bio checks are string matches that become free-forever Python files instead of paid AI tokens, a meaningful per-row saving across hundreds of thousands of rows. The catch he adds: deterministic code is cheaper and easier to audit, but in a CLI it still fails silently ([[concept-silent-failures]]).

## Sources

[[source-eric-nowoslawski-deterministic-scraping]], [[source-eric-nowoslawski-subagent-list-cleaning]] by [[expert-eric-nowoslawski]]; restated in [[source-garrett-wolfe-claude-code-vs-clay]] by [[expert-garrett-wolfe]].

## Related

[[play-cheap-list-processing]] | [[concept-waterfall-enrichment]] | [[tool-html2text]] | [[tool-codex]] | [[concept-data-commoditisation]] | [[concept-silent-failures]] | [[concept-data-vs-reasoning-layer]]
