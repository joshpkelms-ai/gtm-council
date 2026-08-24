---
title: "Play: CRM to ad strategy (audit the CRM, build segmented paid audiences)"
type: play
tags: [play, ai-gtm, automation, agentic, reporting, inbound]
last-updated: 2026-06-12
last-updated-time: 23:10
---

# Play: CRM to ad strategy

> Point a [[tool-claude-code]] skill at your CRM; it audits the data model, maps paid audience segments, and outputs platform-ready campaign plans plus the cleanup needed before launch. From [[expert-andy-toizer]].

## When to use

Standing up or refreshing paid campaigns (Google / LinkedIn / Meta) from CRM data; turning a messy CRM into segmented, activation-ready audiences without manual list-pulling.

## Steps

1. **Connect to the CRM** (e.g. [[tool-hubspot]]).
2. **Audit fields and data model.** The agent reasons through stale lifecycle stages, bad associations, and conflicting records before building anything.
3. **Map paid audience segments**, for example:
   - Tier 1 accounts -> ABM (LinkedIn) and demand capture (Google).
   - Open deals -> buying-committee retargeting / pipeline acceleration.
   - Stale open deals -> nurture + reactivation.
   - Recent signups + form converters -> warm retargeting.
   - Closed Won -> lookalike prospecting (Meta).
   - Closed Won / Lost / Disqualified -> exclusions and suppression.
4. **Build campaign plans** per platform (Google / LinkedIn / Meta).
5. **Draft copy angles by segment.**
6. **Flag cleanup work** before launch.

## Outputs

Audience map, platform campaign plan, activation notes, and a segment CSV/JSON.

## Notes

Exclusions and suppression (Closed Won/Lost) matter as much as targeting. The agent surfaces data-quality issues rather than silently trusting the CRM (a [[concept-claim-tagging]]-style instinct).

## Source

[[source-andy-toizer-crm-ad-strategy-skill]] by [[expert-andy-toizer]].

## Related

[[tool-claude-code]] | [[tool-hubspot]] | [[framework-gtm-brain]] | [[expert-andy-toizer]]
