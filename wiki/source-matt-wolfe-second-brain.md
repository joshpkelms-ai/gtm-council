---
title: "Source: Matt Wolfe -- Build A Second Brain That Remembers Everything"
type: source
tags: [source, reference, ai-gtm, automation, agentic, data]
source-title: "Build A Second Brain That Remembers Everything"
source-url: "https://www.youtube.com/watch?v=yke4fLQUsh4"
source-author: Matt Wolfe
source-published: 2026-05-06
raw-path: "raw/misc/Build A Second Brain That Remembers Everything.md"
last-updated: 2026-06-13
last-updated-time: 12:15
---

# Source: Matt Wolfe -- Build A Second Brain That Remembers Everything

> A long, practical video walkthrough building the Karpathy LLM-wiki pattern end to end. A worked implementation reference for [[concept-llm-wiki-pattern]] (the clipping opens by linking the Karpathy gist). Raw: `raw/misc/`.

## Summary

Wolfe builds a "second brain" knowledge-management system: a chat-able wiki that pulls information on demand, a built-in CRM, a journaling surface that consults the wiki to help with whatever he is working through, and an ingestion pipeline for content saved from around the web (YouTube videos, articles, tweets, podcasts). Everything is queryable from chat or from journaling.

It is the consumer/creator-facing implementation of the same architecture this vault uses: raw captured sources, an LLM-maintained wiki, and chat/query on top, with the LLM doing the filing and cross-referencing.

## Why it matters here

It demonstrates the LLM-wiki pattern as a finished, usable system rather than a sketch, including a CRM and journaling layer, which shows how naturally the pattern extends toward GTM-adjacent uses (relationship memory, decision support). Pairs with the personal-OS instance ([[source-tom-ashworth-personal-os]]) and the originating idea ([[source-karpathy-llm-wiki]]).

## Key takeaways

- A practical, replicable build of the raw -> wiki -> chat pattern.
- Adds a CRM and journaling on top of the knowledge wiki.
- Confirms the pattern is product-shaped, not just a research curiosity.

## Attribution

Matt Wolfe (YouTube). Structural / implementation reference (no practitioner expert page). See [[concept-llm-wiki-pattern]].
