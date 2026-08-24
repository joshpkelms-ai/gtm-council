---
title: Will Jones
type: expert
tags: [expert, ai-gtm, agentic, revops, tool-integration, inbound]
author: Will Jones
last-updated: 2026-08-22
last-updated-time: 12:00
---

# Will Jones

> GTM Operations Associate at Attio. The operator behind the line [[expert-dave-lynch]] calls "the clearest articulation of the GTM engineer role I've heard so far": the job is "less about doing the work directly, and more about directing Agents to do it well." Deployed Intercom's Fin as an always-on inbound SDR on Attio's site, largely himself, by building the context layer first.

## Who he is

Sits in GTM operations at Attio (CRM vendor; ~$116M raised, 8,000+ paying customers as stated in his own account). Notable that his title is **operations, not engineering** - the corpus's cleanest statement of the GTM engineer role comes from someone who does not hold the title. Evidence for the reading that GTM engineering is currently a capability more than a job.

## Core positions

- **Context is the whole job, and it is upstream work.** His number-one piece of advice: "get the context kind of synthesized for an agent." Concretely: point a research agent (he names Claude) at all publicly accessible material - case studies, features, help centre, product pages - and synthesise it into context documents for the agent. This is [[concept-context-assembly]] executed by one person in weeks.
- **Your existing docs are the wrong training set.** Attio's help centre was "basically the service agent's training set" - good at explaining how the product works, weak on unique selling points. Support content does not transfer to a sales agent. A specific, testable failure mode the vault had not previously named.
- **Then close the loop with your own sales data.** Iterate by reading sales calls in the CRM to answer "what actually sells customers on our product", and feed that back. Context work is a loop, not a one-off load.
- **Training persists, so quality stops being variable.** "You can basically train Finn once and your kind of sales quality will always be the same, regardless of like what the customer asks." The argument for agents is consistency, not just coverage.
- **Build for the coverage gap, not a broken motion.** "There wasn't really a problem with our sales motion. It was more like we were trying to look ahead of a curve." The gap was structural: a form needs a human at the end of it, and a 7pm Friday call does not happen. They were missing "an unknown amount of potential prospects."
- **Chat logs are a messaging research instrument.** "Customers don't always use the language that you think they're gonna use." Reading what prospects actually ask tells you what your landing pages are missing. Inbound agent as voice-of-customer capture, feeding [[concept-list-is-the-message]]-style precision back into owned pages.
- **A CRM must be agent-connectable on three surfaces:** built-in agents, [[tool-mcp]] connections (Claude, ChatGPT, Gemini), and an API layer good enough to script actions against. See [[tool-attio]] and [[concept-agent-readiness]].

## What he built

Not a product: the connective layer. Fin writes directly into Attio, Attio writes back into Intercom with CRM data, the two cross-populate, and qualified prospects reach the deal owner instantly rather than being routed through a traditional sales flow. Plus the context documents that make the agent worth connecting, and a feedback loop from chat logs into landing-page copy. The clearest worked example of [[concept-orchestration-layer]] in the corpus.

## Caveats

Self-reported, on a vendor's podcast, alongside the vendor's CPO, with no figures attached to the outcome ("more and more leads", no baseline). Treat results as [ESTIMATED] per [[concept-claim-tagging]]. The *method* is the durable part, and it is corroborated by the independent context-engineering strand ([[expert-jacob-dietle]], [[expert-matteo-tittarelli]]).

## Sources

- [[source-will-jones-attio-fin-sdr]] -- CX Today case study with Paul Adams (Intercom), August 2026.
- Quoted second-hand in [[source-dave-lynch-rise-of-gtm-engineering]].

## Related

[[expert-dave-lynch]] | [[concept-orchestration-layer]] | [[concept-context-assembly]] | [[tool-attio]] | [[tool-mcp]] | [[concept-agent-readiness]] | [[concept-foundations-before-automation]]
