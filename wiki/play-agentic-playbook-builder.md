---
title: "Play: Agentic playbook builder (raw operator notes to structured playbook)"
type: play
tags: [play, ai-gtm, automation, revops, enablement]
last-updated: 2026-06-13
last-updated-time: 09:00
---

# Play: Agentic playbook builder

> A Claude Project (or scheduled Cowork session) that takes raw operator experience, call notes, and field observations and structures them into an execution-ready GTM playbook -- the documentation work that used to take a Saturday, now 30 minutes. The AI holds the structure; the operator brings the truth. [[expert-koen-stam]]'s GTMcraft build; the principle is [[framework-processes-first]] (documentation is the foundation AI amplifies).

## When to use it

You have lived operator knowledge (what is working, what is breaking) but it lives in your head, not in a system a team or an agent can run on. Undocumented process fed to AI returns noise.

## How it works

A Claude Project with fixed instructions enforces a repeatable structure so every playbook comes out the same shape:

- **Intake:** topic and operator problem; company stage (0-2M / 2-5M / 5-10M ARR); known data points or named examples; what is working now vs breaking down.
- **Fixed 3-phase architecture:** Phase 1 CREATE (foundation, days 1-5), Phase 2 OPERATIONALISE (daily execution, days 6-14), Phase 3 SCALE (compound, week 3+) -- four steps per phase, twelve total.
- **Per step:** why it matters, how to execute this week, what good looks like (observable bullets), the common trap with a fix, the AI layer (what the tool does vs where human judgment stays required), and scaling guidance (founder-led / lean team / full GTM).
- **Writing rules baked into the prompt:** declarative cause-to-effect statements, specific day timelines, observable behaviours not opinions, honest gaps acknowledged, and a banned-language list (no em dashes, no hype words, no "it is not X, it is Y" constructions).

A sibling Sales Coaching System project runs the same pattern over call transcripts (connected to [[tool-gong]] or Leexi), scoring SPICED or MEDDICCC per element, citing specific transcript moments, and tracking each coachee's development across sessions so coaching compounds per rep.

## What the operator still owns

The judgment layer: which patterns matter for this rep at this stage, when to push vs build confidence, and the named anecdotes, deals, and outcomes that make a playbook credible rather than generic. The system holds the structure; you bring the truth.

## Why it belongs in the vault

A concrete, copyable instance of structured-prompt documentation as the AI foundation -- the operating layer of [[framework-processes-first]], and a cousin of [[play-case-study-extraction]] (structure first, human supplies the real specifics, no invented detail; see [[concept-claim-tagging]]).

## Related

[[framework-processes-first]] | [[play-case-study-extraction]] | [[concept-claim-tagging]] | [[tool-gong]] | [[tool-claude-code]] | [[expert-koen-stam]]

## Sources

[[source-koen-stam-processes-first-gtmcraft]].
