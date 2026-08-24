---
title: "Source: Andy Toizer -- A Claude Code skill that turns a CRM into ad strategy"
type: source
tags: [source, ai-gtm, automation, agentic, reporting]
source-title: "I built a Claude Code skill that audited our 112k HubSpot contacts for paid ad campaign ideas"
source-url: "[LinkedIn post URL not recorded]"
source-author: Andy Toizer
source-published: unknown
raw-path: raw/Andy Tozier/2.md
last-updated: 2026-06-12
last-updated-time: 23:10
---

# Source: Andy Toizer -- A Claude Code skill that turns a CRM into ad strategy

> LinkedIn post plus an annotated product visual (transcribed) by [[expert-andy-toizer]]. Raw: `raw/Andy Tozier/2.md`.

## Summary

Toizer built a [[tool-claude-code]] skill (`/crm-ad-campaign-builder`) that audited 112k [[tool-hubspot]] contacts for paid ad campaign ideas and found 9 segmented ad audiences in 10 minutes:

- Tier 1 accounts for ABM
- Open deals for buying-committee retargeting
- Stale open deals for nurture + reactivation
- Recent signups + form converters for warm retargeting
- Closed Won / Closed Lost for exclusions + suppression

The agent reasoned through CRM mess (stale lifecycle stages, bad associations, conflicting records) before building audiences. He codified the workflow into a runnable repo. How it works: connects to the CRM, audits fields and data model, maps paid audience segments, builds campaign plans for Google/LinkedIn/Meta, drafts copy angles by segment, and flags cleanup work before launch. Outputs an audience map, platform campaign plan, activation notes, and a segment CSV/JSON. See [[play-crm-to-ad-strategy]].

The visual shows the skill routing CRM data into Google (demand capture, pipeline acceleration, exclusions), LinkedIn (ABM, buying-committee retargeting, signup retargeting), and Meta (warm retargeting, lookalike prospecting, suppression) cards with audience sizes.

## Key takeaways

- A skill can audit a messy CRM and output platform-ready segmented ad strategy. See [[play-crm-to-ad-strategy]].
- Exclusions and suppression (Closed Won/Lost) matter as much as targeting.
- The agent flags data-quality cleanup before launch rather than silently trusting the CRM.

## Attribution

[[expert-andy-toizer]], Head of Growth at Freckle.io, AgentOperator (agentoperator.substack.com). Original LinkedIn post.
