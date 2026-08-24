---
title: "Source: Andrej Karpathy -- From Vibe Coding to Agentic Engineering"
type: source
tags: [source, reference, ai-gtm, agentic, automation]
source-title: "Andrej Karpathy: From Vibe Coding to Agentic Engineering (Sequoia AI Ascent 2026)"
source-url: "https://www.youtube.com/watch?v=96jN2OCOfLs"
source-author: "Andrej Karpathy (interviewed by Stephanie Zhan, Sequoia)"
source-published: 2026-04-29
raw-path: "raw/misc/Andrej Karpathy From Vibe Coding to Agentic Engineering.md"
last-updated: 2026-06-13
last-updated-time: 12:15
---

# Source: Andrej Karpathy -- From Vibe Coding to Agentic Engineering

> Karpathy at Sequoia's AI Ascent 2026 on what changed in the year since he coined "vibe coding". A structural reference for the agentic-engineering ethos under [[concept-borrow-from-engineering]]. Raw: `raw/misc/`.

## Summary

The headline distinction, directly transferable to GTM engineering:

- **Vibe coding raises the floor; agentic engineering preserves the quality bar.** Vibe coding lets anyone build software. Agentic engineering is the discipline of going much faster *without* sacrificing the quality, security, and responsibility that professional work demands. It is an engineering discipline, not a vibe.
- **Agents are jagged, stochastic, powerful "intern entities" (ghosts, not animals).** Extremely capable but they make weird mistakes. His example: an agent tried to cross-correlate Stripe and Google funds by matching email addresses, when those can be arbitrary, exactly the kind of judgment a human must still hold.
- **The human owns spec, taste, judgment, and oversight; the agent fills in the blanks.** You no longer memorise API details (he has forgotten the PyTorch/NumPy minutiae) but you must keep the fundamentals so you ask for the right things. "You can outsource your thinking but never your understanding."
- **The 10x engineer is now an understatement.** The ceiling on agentic-engineering capability is very high; the best peak far beyond 10x.
- **Verifiability makes things tractable.** Verifiable settings let you throw RL (and your own fine-tuning) at a problem; unverifiable work can be approached with a council of LLM judges. Ultimately he thinks almost everything becomes verifiable to some degree, and so automatable, it is a matter of easy vs hard.
- **Hiring should change.** Test agentic-engineering capability with a big, real project ("build a secure Twitter clone, now I will try to break it"), not old-paradigm puzzles. Being AI-native is investing in your setup and getting the most from the tools.

## Why it matters here

GTM engineering is downstream of agentic software engineering ([[concept-borrow-from-engineering]]). The vibe-coding/agentic-engineering split is the same line the GTM corpus draws between fast-but-sloppy automation and disciplined scaling: it rhymes with [[concept-earn-the-right-to-automate]] (don't scale until the quality bar holds), [[concept-silent-failures]] (agents fail in weird, quiet ways), [[concept-specialist-moat]] and [[concept-hybrid-gtm]] (taste and human oversight remain the moat), and "council of LLM judges" prefigures the LLM-as-judge habit in GTM evals.

## Key takeaways

- Agentic engineering = speed without dropping the quality/security bar; you remain responsible.
- Agents are powerful but jagged; humans hold spec, taste, and oversight.
- Outsource thinking, never understanding; keep fundamentals, drop API trivia.
- Verifiability is what makes a task automatable; build verification (judges, tests) for the swishy stuff.

## Attribution

Andrej Karpathy, interviewed by Stephanie Zhan (Sequoia). Structural / meta-reference (ingested as concept material, no practitioner expert page). See [[concept-borrow-from-engineering]], [[concept-llm-wiki-pattern]].
