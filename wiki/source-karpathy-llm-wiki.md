---
title: "Source: Andrej Karpathy -- LLM Wiki / LLM Knowledge Bases"
type: source
tags: [source, reference, ai-gtm, automation, agentic, data]
source-title: "LLM Wiki (gist idea file) + LLM Knowledge Bases (tweet)"
source-url: "https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f | https://x.com/karpathy/status/2039805659525644595"
source-author: Andrej Karpathy
source-published: unknown
raw-path: "raw/misc/# Andrej Karpathy LLM Wiki.md, raw/misc/Andrej Karpathy - LLM Knowledge Bases TW.md"
last-updated: 2026-06-13
last-updated-time: 12:15
---

# Source: Andrej Karpathy -- LLM Wiki / LLM Knowledge Bases

> The originating statement of the pattern this vault uses, distilled into [[concept-llm-wiki-pattern]]. Ingested as one structural reference body (the gist idea file plus the tweet that announced it). Raw: `raw/misc/`.

## What this is

- **LLM Wiki (gist)** -- an "idea file" meant to be pasted into a coding agent (Codex, Claude Code, OpenCode) to bootstrap a personal knowledge base. Lays out the core idea (a persistent, compounding LLM-maintained wiki vs query-time RAG), the three-layer architecture (raw / wiki / schema), and the three operations (Ingest / Query / Lint). Use cases span personal, research, reading a book, business/team, due diligence.
- **LLM Knowledge Bases (tweet)** -- Karpathy's shorter public note on the same practice: index sources into `raw/`, have an LLM "compile" a markdown wiki with summaries, backlinks, and concept articles; use Obsidian as the IDE frontend; ask complex questions against the wiki (his research wiki was ~100 articles / ~400K words); file outputs back in; run LLM "health checks" to lint. "You rarely ever write or edit the wiki manually, it's the domain of the LLM. I think there is room here for an incredible new product."

## Why it matters here

This is the literal blueprint for gtm-council: the raw / wiki / schema layering, the Ingest / Query / Lint operations, the "LLM owns the wiki, human curates and questions" division, and filing good answers back as pages. It is also the parent pattern of the GTM context-repo frameworks ([[framework-gtm-brain]], [[framework-strategy-as-repo]], [[framework-ai-employee-loop]]) and the context-OS work of [[expert-jacob-dietle]], who calls his system "a version of the larger context graph Karpathy tweeted about".

## Key takeaways

- Compile knowledge once and keep it current; do not re-derive it on every query.
- Three layers: immutable raw sources, an LLM-maintained wiki, a schema config that enforces discipline.
- Three operations: Ingest, Query (file answers back), Lint.
- Obsidian as IDE, LLM as programmer, wiki as codebase.

## Attribution

Andrej Karpathy. Structural / meta-reference (per CLAUDE.md, ingested as a concept, not given a practitioner expert page). See [[concept-llm-wiki-pattern]].
