---
title: "Source: Dave Lynch -- The rise of GTM engineering"
type: source
tags: [source, ai-gtm, automation, revops, tool-integration]
source-title: "The rise of GTM engineering"
source-url: "https://ideas.fin.ai/p/the-rise-of-gtm-engineering"
source-author: Dave Lynch
source-published: 2026-06-04
raw-path: raw/Clippings/The rise of GTM engineering.md
last-updated: 2026-06-12
last-updated-time: 12:00
---

# Source: Dave Lynch -- The rise of GTM engineering

> Essay on the Fin (Intercom) ideas blog by [[expert-dave-lynch]]. Raw: `raw/Clippings/The rise of GTM engineering.md`. The clearest first-hand account in this corpus of standing up a GTM engineering function. Anchors [[concept-orchestration-layer]].

## Summary

AI and coding agents make it cheap and fast to build targeted internal solutions to GTM problems, giving an edge over teams on bloated off-the-shelf SaaS. Lynch's team at Fin is a dedicated GTM-engineering function, already beating commercial targets with adoption beyond expectations.

- **The power of the pair.** Pair an AI-forward generalist engineer with a domain expert who knows the problem and the org. This shifts the question from "what can a team achieve" to "what can one engineer achieve" -- a lot more than before. Built an AEO engine (grew bot-sourced pipeline; see [[concept-aeo]]) and an outbound engine on the same model.
- **Build bespoke, but not everything.** SaaS isn't dead; it's disrupted. Keep buying systems of record (Salesforce, Stripe, Fin) -- deep, embedded, unwise to rebuild. What's newly buildable is the layer above: the orchestration/customization that connects systems and fills the gaps for the rep, marketer, or CSM. See [[concept-orchestration-layer]].
- **Evidence.** A "cockpit" over Outreach + data warehouse + internal infra turned ideas into pipeline ($1.2M generated, tracking to $5M by year-end, no migration); a 3-week internal tool replaced a vendor product under evaluation. Will Jones (GTM ops, Attio) implemented Fin for Sales largely himself by turning help-center content, testimonials, and call transcripts into context docs, then building and testing a Sales Agent in weeks -- describing his job as "directing Agents to do it well" (the corpus's clearest articulation of the GTM engineer role).
- **Jevons paradox (via Nicolas Sharp, Attio):** as AI gets more capable, demand for people who build and operate it grows, not shrinks.

## What he's nervous about

Honest about the ambiguity: are the cockpits durable foundations or sophisticated throwaways? As tools get good enough for everyone to self-serve, his team likely gets smaller and less engineering-heavy. Core software principles still apply: you throw away half of what you try, while a sales team needs pipeline this quarter. Nicolas Sharp's answer: "build for the flex, not the forecast" -- don't predict 18 months out, build an org agile enough that a 50%-wrong vision doesn't matter.

## Key takeaways

- The role is real: embed a builder next to a domain expert, fast feedback loop, get out of the way.
- The defensible work is the orchestration layer between systems of record, now buildable in weeks. See [[concept-orchestration-layer]].
- Maps onto Sachin Jha's Layer 3 ([[framework-three-layer-gtm]]) and the broader [[concept-borrow-from-engineering]] thesis.

## Attribution

[[expert-dave-lynch]], Fin (fin.ai / Intercom). ideas.fin.ai. References Nicolas Sharp and Will Jones of Attio.
