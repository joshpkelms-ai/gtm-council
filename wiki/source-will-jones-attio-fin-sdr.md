---
title: "Source: Will Jones & Paul Adams -- How Attio turned Fin into an always-on sales rep"
type: source
tags: [source, ai-gtm, agentic, inbound, tool-integration, revops]
source-title: "How CRM Vendor Attio Turned Intercom's Fin AI Agent Into an Always-On Sales Rep"
source-url: "https://www.listennotes.com/podcasts/cx-today/how-crm-vendor-attio-turned-JBhlDE2oR-q/"
source-author: "Will Jones (Attio), Paul Adams (Intercom); host Nicole Willing"
source-publisher: "CX Today"
source-published: 2026-08-03
raw-path: "raw/Clippings/How CRM Vendor Attio Turned Intercom's Fin AI Agent Into an Always-On Sales Rep.md"
last-updated: 2026-08-22
last-updated-time: 12:00
---

# Source: How Attio turned Fin into an always-on sales rep

> CX Today case study, 18 minutes. [[expert-will-jones]] (GTM Operations Associate, Attio) with Paul Adams (CPO, Intercom). **The primary source behind the second-hand quote in [[source-dave-lynch-rise-of-gtm-engineering]].** Raw: `raw/Clippings/How CRM Vendor Attio Turned Intercom's Fin AI Agent Into an Always-On Sales Rep.md` (complete transcript, naturalised from the source WEBVTT - see the provenance note there for the conventions and the three transcription footnotes).
>
> Its value to this vault is not the vendor story. It is the corpus's most concrete worked example of [[concept-orchestration-layer]]: an operator naming, step by step, what he actually built between two bought systems.

## Why it matters here

[[expert-dave-lynch]] built a large claim on one Jones line ("directing Agents to do it well") without showing the work behind it. This source shows the work. It converts the vault's most abstract concept - "build the layer above your systems of record" - into an itemised build.

## The build, itemised

Attio bought both systems of record: its own CRM and Intercom's Fin. What Jones built between them:

1. **Context documents.** Point a research agent (he names Claude) at all publicly accessible material - case studies, features, help centre, product pages - and synthesise it into context docs for the agent. His stated number-one piece of advice.
2. **Two-way data wiring.** Fin writes into Attio; Attio writes back into Intercom with CRM data. "They're basically cross-populating each other and sharing information."
3. **Routing logic.** Qualified prospects reach the deal owner instantly "rather than having to be routed through kind of a traditional sales flow."
4. **A re-engagement rule.** Prospects who leave an email without completing a conversation get automated follow-ups.
5. **A feedback loop back into owned assets.** Read the chat logs, find the language prospects actually use, retune the landing pages.
6. **A second loop back into the agent.** Read sales calls in the CRM to find "what actually sells customers on our product", feed that back into the agent's context.

None of that is a product. All of it is connective tissue plus context plus rules. That is the orchestration layer, concretely.

## Key claims

- **Not a broken motion, a coverage gap.** "There wasn't really a problem with our sales motion. It was more like we were trying to look ahead of a curve." A form is only as available as the human behind it; a 7pm Friday call does not happen. They were missing "an unknown amount of potential prospects."
- **Support content is the wrong training set for a sales agent.** The help centre was "basically the service agent's training set" - fine on how the product works, weak on unique selling points. A specific failure mode the vault had not named.
- **Consistency, not just coverage.** "The training is permanent... you can basically train Finn once and your kind of sales quality will always be the same."
- **Agent-readiness has three surfaces** (Jones on what a CRM must offer): built-in agents, [[tool-mcp]] connections, and a scriptable API layer. Feeds [[concept-agent-readiness]] and [[tool-attio]].
- **Adams: single agent, single customer record.** Multiple agents from different vendors "have different context... different memory, and it'll end up being a big mess", recreating the "I already told the other person" experience. Note this is also an argument for buying more Intercom.
- **Adams on scale of change.** "AI is just way, way bigger than either mobile as a technology cycle or the internet itself. Because AI does work" - prior cycles helped us do existing things better, whereas AI does the work itself. Intercom is "fully Claude Coded" internally.

## The disagreement inside the episode

The two guests contradict each other on the vault's single strongest consensus, and neither notices.

- **Adams: "Don't wait."** He explicitly classifies "our data isn't ready" and "we first have to sort out this organizational thing between these two teams" as excuses. "If you're kind of thinking about it, you're already way too late."
- **Jones: do the context work first.** His entire contribution is that the build only worked because he assembled and corrected the context before connecting anything, and that the obvious existing corpus was the wrong one.

This is a live challenge to [[concept-foundations-before-automation]] (Moscatiello: "AI is a multiplier of whatever foundation exists"), [[framework-three-layer-gtm]] (Jha) and [[framework-processes-first]] (Stam). **Adjudication:** the council wins, and the episode supplies its own evidence. Adams is the vendor CPO whose commercial interest is shortening the sales cycle, arguing from no build; Jones is the operator who did the build, and his account is a foundations-first account. Adams is also attacking a real failure mode - "data isn't ready" used as indefinite deferral - which the council should concede. The defensible line is Jones's: do the context work, but scope it to the one motion you are automating rather than boiling the CRM. Adams's advice is right about the disease and wrong about the cure.

## Caveats

Vendor podcast, vendor CPO in the room, no figures on the outcome ("more and more leads", no baseline, no conversion or pipeline number). Treat all results as [ESTIMATED] per [[concept-claim-tagging]]. Adams's Anthropic/Clay/Attio name-drop is customer-list marketing, not evidence. The method is what survives; the outcome claims do not.

## Attribution

[[expert-will-jones]], Attio. Paul Adams, Intercom. Hosted by Nicole Willing, CX Today, 3 August 2026.

## Related

[[concept-orchestration-layer]] | [[expert-will-jones]] | [[expert-dave-lynch]] | [[tool-attio]] | [[concept-context-assembly]] | [[concept-foundations-before-automation]] | [[tool-mcp]] | [[concept-agent-readiness]] | [[concept-claim-tagging]]
