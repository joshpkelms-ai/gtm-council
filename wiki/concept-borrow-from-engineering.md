---
title: "Concept: Borrow from software engineering (GTM is ~18 months behind)"
type: concept
tags: [concept, ai-gtm, automation, agentic, tool-integration]
last-updated: 2026-06-13
last-updated-time: 12:15
---

# Concept: Borrow from software engineering

> Software engineers are roughly 18 months ahead of GTM on coding agents. The fastest way forward for GTM engineering is to steal their patterns: runtime docs retrieval, version control, repos, skills, and provenance discipline.

## The idea

[[expert-andy-toizer]]: "I steal most of my GTM ideas from software engineers, because they're about 18 months ahead of us on coding agents." The concrete example: engineers have Context7, 9,000+ libraries of always-current docs their agents pull at runtime. The GTM stack was not in it, so he built the GTM equivalent ([[tool-gtm-docs-registry]]).

## The pattern across the corpus

Several GTM-engineering ideas are lifts from software engineering practice:

- **Runtime docs retrieval** (Context7 -> GTM Docs Registry). See [[concept-agent-readiness]].
- **Version-controlled assets in repos** rather than decks. See [[framework-strategy-as-repo]], [[framework-gtm-brain]].
- **Skills as committed, namespaced folders.** See [[concept-skill-namespacing]].
- **Provenance and review gates** (approved-claims, needs-review). See [[concept-claim-tagging]].
- **DRY / functions as single source of truth** (call not copy). See [[concept-gtm-functions]].

- **Build the connective layer, buy the systems of record** (the buy/build line software settled long ago). See [[concept-orchestration-layer]].

## Why it matters

GTM engineering as a discipline is downstream of agentic software engineering. Watching what works for engineers is a reliable forward indicator of what is about to work for GTM.

## The discipline being borrowed (Karpathy)

The source discipline GTM is copying has its own name. [[source-karpathy-vibe-coding-agentic-engineering]] distinguishes **vibe coding** (raising the floor; anyone can build) from **agentic engineering** (preserving the quality bar while going much faster, and remaining responsible for the result). The transferable rules:

- Agents are jagged, powerful "intern entities" that make weird mistakes; the human owns spec, taste, judgment, and oversight while the agent fills in the blanks.
- "Outsource your thinking but never your understanding": drop the API trivia, keep the fundamentals.
- Verifiability is what makes a task automatable; build verification (tests, a council of LLM judges) for the swishy work.

This is the engineering-side root of GTM's own [[concept-earn-the-right-to-automate]] (hold the quality bar before scaling), [[concept-silent-failures]] (jagged, quiet agent errors), and [[concept-specialist-moat]] / [[concept-hybrid-gtm]] (taste and oversight as the moat). The wider knowledge-work analogue is [[concept-llm-wiki-pattern]], also Karpathy.

## The counterweight

[[framework-three-rs-enablement]] (Mercy Bell) inverts the slogan: don't only borrow agent patterns for machines; apply the same rigour to developing the humans who still run GTM.

## Sources

[[source-andy-toizer-gtm-docs-registry-launch]] by [[expert-andy-toizer]]; [[source-karpathy-vibe-coding-agentic-engineering]] by Andrej Karpathy.

## Related

[[tool-gtm-docs-registry]] | [[concept-agent-readiness]] | [[framework-strategy-as-repo]] | [[framework-gtm-brain]] | [[concept-skill-namespacing]] | [[concept-llm-wiki-pattern]] | [[concept-earn-the-right-to-automate]] | [[concept-silent-failures]] | [[expert-andy-toizer]]
