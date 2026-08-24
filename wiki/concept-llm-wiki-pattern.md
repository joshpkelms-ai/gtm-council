---
title: "Concept: The LLM-wiki pattern (raw / wiki / schema)"
type: concept
tags: [concept, reference, ai-gtm, automation, agentic, data]
last-updated: 2026-06-13
last-updated-time: 12:15
---

# Concept: The LLM-wiki pattern

> A persistent, compounding knowledge base an LLM builds and maintains for you, instead of re-deriving answers from raw documents on every query. The structural spine this very vault (gtm-council) is built on. Andrej Karpathy's pattern.

## The core idea

Most LLM-plus-documents setups are RAG: upload files, retrieve chunks at query time, generate an answer. Nothing accumulates; the model rediscovers knowledge from scratch every time. The LLM-wiki inverts this: the LLM **incrementally compiles and maintains a persistent wiki** of interlinked markdown that sits between you and the raw sources. Add a source and the LLM reads it, extracts the key information, updates entity and topic pages, flags contradictions, and strengthens the synthesis. Knowledge is compiled once and kept current. The wiki is a compounding artifact: cross-references already there, contradictions already flagged.

You own sourcing, exploration, and asking good questions; the LLM does the grunt work (summarising, cross-referencing, filing, bookkeeping). "Obsidian is the IDE; the LLM is the programmer; the wiki is the codebase."

## Three layers

- **raw/** -- the curated, immutable source documents. The LLM reads, never edits. Source of truth.
- **wiki/** -- the LLM-generated and LLM-maintained markdown: summaries, entity/concept pages, syntheses, an index. The LLM owns this layer.
- **schema** -- a config document (CLAUDE.md for Claude Code, AGENTS.md for Codex) defining structure, conventions, and the workflows for ingesting, answering, and maintaining. This is what makes the LLM a disciplined wiki maintainer rather than a generic chatbot. Co-evolved over time.

## Three operations

- **Ingest** -- drop a source in raw/, the LLM reads it, surfaces takeaways, writes a summary, updates the index and the relevant entity/concept pages (a single source may touch 10-15 pages), and appends to a log. One at a time with supervision, or batch with less.
- **Query** -- ask against the wiki; the LLM finds relevant pages and answers with citations. Good answers are filed back as new pages so explorations compound.
- **Lint** -- periodic health check: contradictions, stale claims, orphan pages, missing concept pages or cross-references, gaps a web search could fill.

## Why it is here

This is the exact architecture and operating model of gtm-council (see this vault's `CLAUDE.md` and the Ingest / Query / Lint operations). It is also the family these GTM frameworks belong to: [[framework-gtm-brain]] (Toizer) and [[framework-strategy-as-repo]] (Waxman) are domain-specific LLM-wikis for GTM context; [[framework-ai-employee-loop]] (Nowoslawski) builds and refreshes a company brain on the same principle; [[concept-context-assembly]] (Tittarelli/Dietle) is the data-layer discipline that keeps the raw layer trustworthy. [[expert-jacob-dietle]] explicitly calls his context OS "a version of the larger context graph Karpathy tweeted about". Worked instances: [[source-tom-ashworth-personal-os]] (a personal life-OS in a git repo) and [[source-matt-wolfe-second-brain]] (a chat-able wiki with CRM and journaling).

## Sources

[[source-karpathy-llm-wiki]] (the idea file and the originating tweet). Structural reference, not a GTM practitioner source.

## Related

[[framework-gtm-brain]] | [[framework-strategy-as-repo]] | [[framework-ai-employee-loop]] | [[concept-context-assembly]] | [[concept-borrow-from-engineering]] | [[source-tom-ashworth-personal-os]] | [[source-matt-wolfe-second-brain]] | [[source-karpathy-llm-wiki]] | [[tool-claude-code]] | [[tool-codex]]
