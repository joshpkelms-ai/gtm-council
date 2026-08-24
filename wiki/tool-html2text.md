---
title: "Tool: html2text"
type: tool
tags: [tool, enrichment-workflow, data, automation]
last-updated: 2026-06-12
last-updated-time: 23:40
---

# Tool: html2text

> Open-source HTML-to-text converter used to extract page content for free, the deterministic first step before any paid scraper or LLM. Anchor tool for [[concept-deterministic-first]].

## What it is

A free, open-source library that converts HTML into plain text. For most "I just want the text on this page" jobs (homepage and footer content), it is enough. Paid scrapers (ZenRows, Firecrawl) earn their money only on genuinely hard targets: heavy anti-bot, JS-gated content, sites that fight you. A reference copy of the project also sits in `raw/misc/html2text 2025.4.15.md`.

## Why it matters in GTM

It is the cheapest rung of [[play-cheap-list-processing]]: pull website text for thousands of companies at $0, then score with deterministic keyword matching rather than an LLM. [[expert-eric-nowoslawski]] crawled thousands of sites this way for near-nothing, with [[tool-claude-code]] orchestrating in goal mode overnight. Note the limit raised by commenters: many modern JS-heavy sites need a headless-browser fallback for content that is not in the initial HTML.

## Source

[[source-eric-nowoslawski-deterministic-scraping]] by [[expert-eric-nowoslawski]].

## Related

[[concept-deterministic-first]] | [[play-cheap-list-processing]] | [[tool-claude-code]]
