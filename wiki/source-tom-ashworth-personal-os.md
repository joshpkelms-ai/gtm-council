---
title: "Source: Tom Ashworth -- Running my life from a git repo + Notes on my AI tools/workflow"
type: source
tags: [source, reference, ai-gtm, automation, agentic]
source-title: "Running my life from a git repo; Notes on my AI tools + workflow"
source-url: "https://tgvashworth.com/2026/05/24/running-my-life-from-a-git-repo.html | https://tgvashworth.com/2026/01/08/notes-on-my-ai-tools-workflow.html"
source-author: Tom Ashworth (tgvashworth)
source-published: "2026-05-24; 2026-01-08"
raw-path: "raw/Clippings/Running my life from a git repo.md, raw/Clippings/Notes on my AI tools + workflow.md"
last-updated: 2026-06-13
last-updated-time: 12:15
---

# Source: Tom Ashworth -- Running my life from a git repo + Notes on my AI tools/workflow

> A worked personal instance of [[concept-llm-wiki-pattern]], plus a practical Claude Code workflow note. Ingested as one structural-reference body (same author, same theme). Raw: `raw/Clippings/`.

## Summary

**Running my life from a git repo.** Inspired by Karpathy's LLM Wiki, Ashworth runs the operational state of his life as plain markdown in a single git repo that [[tool-claude-code]] reads and writes. No app, no database, just files and conventions. He interacts via the terminal, Claude Code on the web (phone), and GitHub Actions for scheduled jobs while he sleeps; Obsidian/VS Code for direct edits. The repo's top level:

- `CLAUDE.md` (entrypoint, loaded every session, `@`-imports the rest), `AGENTS.md` (the operating manual), `INDEX.md` (map of active projects), `MEMORY.md` (cross-session notes), `TODOS.md`, `LOG.md` (append-only event log).
- `projects/`, `knowledge/` (the wiki: sources, summaries, topic pages), `inbox/` (markdown view of email), `thinking/`, `dreams/` (nightly agent observations), `scripts/`.

It extends the LLM-wiki beyond knowledge into operational state, and uses scheduled agents to do maintenance autonomously.

**Notes on my AI tools + workflow.** A grounded "how I actually work with Claude" update. Deliberately vanilla (echoing Boris Cherny's setup): VS Code as a normal IDE, one or more Claude Code instances per worktree (often one for research, one for writing code), Claude Code in GitHub Actions for async work, Claude Code for Web for trivial tasks and research. He wraps recurring functionality in plugins and has folded voice and images into the daily loop.

## Why it matters here

The repo structure (`CLAUDE.md` + `INDEX.md` + `LOG.md` + a `knowledge/` wiki, with append-only logging and an operating manual) is the same scaffolding gtm-council uses, and the same one the GTM context-repo frameworks adopt ([[framework-gtm-brain]], [[framework-strategy-as-repo]]). It is the clearest demonstration that the pattern generalises from knowledge to live operational state, and that scheduled agents can run the maintenance. The vanilla-Claude-Code workflow (worktrees, research/writing split, GitHub Actions, plugins) is the practical substrate under the GTM hub bet ([[tool-claude-code]]).

## Key takeaways

- The LLM-wiki pattern extends to operational state (todos, inbox, projects), not just knowledge.
- A small set of conventions plus an entrypoint that auto-loads context (CLAUDE.md `@`-imports) beats an app.
- Scheduled agents (GitHub Actions) do the unglamorous maintenance.
- A productive setup can be "vanilla": worktrees, a research/writing split, plugins for repeated jobs.

## Attribution

Tom Ashworth (tgvashworth.com). Structural / meta-reference (ingested as concept material; no practitioner expert page). See [[concept-llm-wiki-pattern]], [[tool-litprompt]] (his prompt-preprocessing tool).
