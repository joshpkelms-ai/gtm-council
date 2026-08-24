---
title: "Concept: Adoption as prioritisation"
type: concept
tags: [concept, ai-gtm, agentic, automation, revops]
last-updated: 2026-06-13
last-updated-time: 09:00
---

# Concept: Adoption as prioritisation

> [[expert-shashank-khanna]] (Head of GTM Engineering, Vanta), documented by [[expert-noah-adelstein]]: of all the workflows that could be automated, which are actually worth the team's time? Stop guessing. Make agent-building a company-wide capability, then let real adoption tell you which ideas deserve production-grade engineering.

## The problem it solves

A GTM Engineering team supporting a much larger sales org faces infinite candidate workflows and finite engineering hours. The three sources of ideas -- leadership, the GTMEs themselves, and reps -- have a ranking problem: rep ideas can be the most impactful but it is hard to tell up front which will scale across the team. Hundreds of GTME hours routinely go into projects that solve no real problem or get no adoption.

## The mechanism

1. **Democratise building.** Give every rep a no-code agent builder (Vanta used [[tool-dust]]) on top of gated, clean data, so anyone can prototype in an afternoon.
2. **Instrument usage.** The central team watches admin analytics: who builds what, which agents spread, which workflows emerge as candidates.
3. **Productionise the winners.** Engineering time goes only to workflows with validated, organic demand. At Vanta the surfaced winners were a support copilot (so popular a human now manages it near full-time), a merged account-research/prioritisation/messaging agent ("Cantaloupe 2.0"), competitor monitoring, and a recruiting copilot.

The result: GTM Engineering becomes a team that ships agents with proven demand rather than guessed-at demand -- the first systematic, bottoms-up way of sourcing GTME use cases. The play is written up at [[play-adoption-driven-roadmap]].

## Preconditions

- **Data foundation first.** Agents are only as good as their data; Vanta built custom MCPs on top of [[tool-gong]] and Snowflake to gate access and remove garbage (see [[concept-context-assembly]], [[concept-silent-failures]]).
- **A builder culture.** Enablement plus public recognition (the CRO's weekly shoutouts) activates the early adopters who lead AI experimentation.

## Relationship to the cluster

This is the discovery-side complement to [[concept-earn-the-right-to-automate]]: rather than one team proving a motion manually, the whole org runs cheap experiments and adoption is the proof. Both reach the same rule -- only build production systems around validated demand.

## Sources

[[source-noah-adelstein-vanta-dust-agent-builders]] ([[expert-noah-adelstein]], featuring [[expert-shashank-khanna]]).

## Related

[[play-adoption-driven-roadmap]] | [[tool-dust]] | [[concept-earn-the-right-to-automate]] | [[concept-context-assembly]] | [[concept-gtm-functions]]
