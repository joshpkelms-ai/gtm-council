---
title: "Framework: Sales orchestration (the layer before execution)"
type: framework
tags: [framework, outbound, automation, signal-based, revops, sequencing, linkedin, inbound]
last-updated: 2026-06-13
last-updated-time: 13:00
---

# Framework: Sales orchestration

> Treat coordination as an engineering problem, not a management one. Sales orchestration is a unified logic layer that sits *before* execution, deciding how signals, data, tasks, and people move through the GTM system so prospects get consistent touchpoints instead of accidental spam. From the HeyReach blog ([[expert-ilija-stojkovski]], [[expert-nada-komnenic]]).

## The problem it solves

Past ~50 employees, systems stop talking and people accidentally spam the same prospect (SDR connection request, AE "circling back", marketing case study, CEO DM, all in one week). "You don't need more leads. You need fewer blockers." Reps sell only ~28% of the time; the rest is coordination chaos. The fix is not more meetings, checklists, or required CRM fields (more process makes it worse); it is engineering the flow. The same shift names the failure on the outbound side: "Most outbound teams don't have a signal problem. They have an orchestration problem."

## Five design principles

1. **Flow over silo.** Build for the end-to-end journey, not handoffs. Pricing-page view triggers sales engagement (intent via [[tool-rb2b]]); a positive LinkedIn reply pauses the email sequence and starts discovery prep.
2. **Automate decisions: score, route, engage.** Speed-to-lead is decisive (reply in 5 minutes = ~8x conversion vs 5-24 hours; B2B average is ~42 hours). Form at 2pm -> Clay enriches in 30s -> Make scores ICP fit and routes -> SDR has a research brief by 2:03pm.
3. **Cross-functional triggers (SDR <-> AE <-> CSM).** A positive reply auto-creates discovery prep with history attached; a closed deal hands CS full context with no briefing; deployment fires expansion workflows.
4. **Agent-driven architecture.** Logic agents handle routine decisions consistently: parse "not until Q2", extract the timing objection, schedule a March follow-up, tag the lead, instantly.
5. **(Systems thinking throughout.)** The difference from task automation is designing for the whole customer journey, not optimising isolated activities.

## Core system components

- **Information flows** -- form capture triggers enrichment + routing in one process; every lead enters with full context attached.
- **Task flows** -- follow-ups, sequences, scheduling fire on prospect behaviour, not human memory.
- **AI agent flows** -- event-triggered decision-makers that read a response, reason over predefined logic, and act at machine speed.

## The signal routing engine (execution side)

When signals (funding, job changes, tech installs, enrichment, CRM scores) scale faster than the systems controlling them, trigger-based automation breaks: duplicate outreach, conflicting messages, overloaded sender seats, account risk. Before any signal reaches a LinkedIn sender, route it through a six-step engine:

1. **Validate** -- is the signal complete, accurate, usable?
2. **Dedupe** -- is another workflow/sender already engaging this account?
3. **Prioritise** -- which signal actually matters right now?
4. **Route** -- which sender, seat, or playbook fits this lead?
5. **Pace** -- can the LinkedIn accounts safely handle this volume today (sender health)?
6. **Monitor** -- is the system behaving, or quietly failing at scale?

## Where it sits in the corpus

This is the GTM-process counterpart to [[concept-orchestration-layer]] (Lynch's *tool*-layer "buy the systems of record, build the connective layer"): same instinct, applied to the movement of leads and touchpoints across teams and channels. The routing engine is the operational answer to [[concept-signal-vs-intent]] and [[framework-signal-intelligence-layer]] (Jha): once you stop hoarding signals, you need a layer that decides which to act on and how. "Monitor / quietly failing at scale" is [[concept-silent-failures]] (Wolfe) stated for outbound. The dedupe-and-pace discipline protects deliverability the way [[concept-deterministic-first]] protects spend.

## Sources

[[source-heyreach-sales-orchestration]] ([[expert-ilija-stojkovski]]) and [[source-heyreach-signal-routing-engine]] ([[expert-nada-komnenic]]), both on the HeyReach blog. Tool: [[tool-heyreach]].

## Related

[[concept-orchestration-layer]] | [[concept-signal-vs-intent]] | [[framework-signal-intelligence-layer]] | [[concept-silent-failures]] | [[tool-heyreach]] | [[tool-rb2b]] | [[tool-clay]] | [[concept-list-is-the-message]]
