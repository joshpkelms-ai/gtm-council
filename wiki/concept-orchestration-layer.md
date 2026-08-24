---
title: "Concept: Build the orchestration layer, buy the systems of record"
type: concept
tags: [concept, ai-gtm, automation, tool-integration, revops]
last-updated: 2026-06-13
last-updated-time: 13:00
---

# Concept: Build the orchestration layer

> [[expert-dave-lynch]] (Fin): SaaS isn't dead, but the buy/build line moved. Keep buying systems of record; build the orchestration layer above them -- the connective tissue that fills the gaps and shapes the workflow around the rep, marketer, or CSM.

## The idea

Foundational platforms (CRM, payments, customer-communication) are deep, broad, embedded systems of record -- unwise to rebuild ("keep buying Salesforce, keep buying Stripe"). What's newly cheap to build, thanks to AI and coding agents, is the layer above: the customization that connects these systems and fills the gaps between them. That used to need a vendor relationship, a six-month implementation, and a dedicated admin; now it needs a strong data foundation, a GTM engineer, and a couple of weeks on a clear problem.

## Why it's defensible now

The orchestration layer is where bespoke beats off-the-shelf: you find the gaps, ship something tuned to your exact needs, and turn ideas into pipeline without a migration or a new tool to learn. Reported at Fin: an outbound "cockpit" over Outreach + warehouse + internal infra ($1.2M pipeline, tracking to $5M); a 3-week internal build that replaced a vendor product under evaluation.

## How to staff it

Pair an AI-forward generalist engineer with a domain expert embedded in the workflow. The question shifts from "what can a team achieve" to "what can one engineer achieve". This is Layer 3 of [[framework-three-layer-gtm]] and a direct instance of [[concept-borrow-from-engineering]] (steal software's agent patterns for GTM).

## The honest caveats

Are the cockpits durable foundations or sophisticated throwaways? As tools get good enough for everyone to self-serve, the team likely shrinks and de-engineers. "Build for the flex, not the forecast" (Nicolas Sharp, Attio): don't predict 18 months out, build an org agile enough that a half-wrong vision doesn't sink you. Core software-delivery principles still apply -- you throw away half of what you try.

## At the tool layer

[[expert-sachin-jha]] makes the same move concretely: keep Clay as the data layer, but move orchestration and reasoning to a layer you own (Claude Code / a Claude Project) rather than renting it inside a vendor's table. That is [[concept-data-vs-reasoning-layer]] -- the tool-level expression of buying systems of record and building the connective layer above.

## At the GTM-process layer

The same "build the connective layer" instinct, applied to the movement of leads, tasks, and touchpoints across teams and channels rather than to tools, is [[framework-sales-orchestration]] (HeyReach): a logic layer that sits before execution so signals are validated, deduped, prioritised, routed, and paced instead of colliding into accidental spam.

## Sources

[[source-dave-lynch-rise-of-gtm-engineering]] by [[expert-dave-lynch]]; [[source-sachin-jha-clay-to-claude-code]] by [[expert-sachin-jha]] (the tool-layer instance).

## Related

[[concept-borrow-from-engineering]] | [[concept-data-vs-reasoning-layer]] | [[framework-three-layer-gtm]] | [[framework-sales-orchestration]] | [[concept-agentic-sourcing]] | [[tool-mcp]] | [[expert-dave-lynch]]
