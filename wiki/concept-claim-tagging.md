---
title: "Concept: Claim tagging (provenance discipline for AI-built strategy)"
type: concept
tags: [concept, ai-gtm, data, messaging]
last-updated: 2026-06-12
last-updated-time: 22:30
---

# Concept: Claim tagging

> Tag every claim in an AI-built strategy document with its confidence and provenance: [VERIFIED], [INFERRED], [ESTIMATED], [UNAVAILABLE]. A blank beats a hallucination.

## The discipline

[[expert-jared-waxman]] tags every claim in repo-based GTM strategy documents with one of four labels:

- **[VERIFIED]** -- backed by a source (e.g. a real customer quote).
- **[INFERRED]** -- reasoned from available evidence.
- **[ESTIMATED]** -- a best-guess figure, flagged as such.
- **[UNAVAILABLE]** -- the data does not exist or was not found. Leave it blank-but-labelled rather than fabricate.

"That last tag is the discipline. A blank beats a hallucination, every time."

## Why it matters

It makes AI-generated research trustworthy and diffable: a reader knows what to rely on and what to chase. It is the trust layer that lets [[framework-strategy-as-repo]] compound, since downstream tools and hires can act on confidence levels rather than treating all text as equally certain.

## The same discipline elsewhere

The principle recurs across the corpus: [[framework-gtm-brain]] (Toizer) separates product-truth from aspiration and signs off "approved-claims"; [[play-case-study-extraction]] (Tittarelli) marks any unsourced number `[METRIC NEEDED]` rather than inventing it; [[concept-context-assembly]] (Tittarelli) resolves and sources data upstream before the model reads it. Different surfaces, one rule: never let unsourced content pass as fact.

## Source

[[source-jared-waxman-strategy-in-repos]] by [[expert-jared-waxman]].

## Related

[[framework-strategy-as-repo]] | [[framework-gtm-brain]] | [[play-case-study-extraction]] | [[concept-context-assembly]] | [[expert-jared-waxman]]
