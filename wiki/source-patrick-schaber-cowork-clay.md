---
title: "Source: Patrick Schaber -- Claude Cowork + Clay has evolved go-to-market operations"
type: source
tags: [source, ai-gtm, automation, enrichment, tool-integration]
source-title: "Claude Cowork + Clay has evolved go-to-market operations"
source-url: "https://patrickschaber.substack.com/p/claude-cowork-clay-has-evolved-go"
source-author: Patrick Schaber
source-published: 2026-04-12
raw-path: raw/Clippings/Claude Cowork + Clay has evolved go-to-market operations.md
last-updated: 2026-06-12
last-updated-time: 14:30
---

# Source: Patrick Schaber -- Claude Cowork + Clay

> Approachable AI newsletter post by [[expert-patrick-schaber]]. Raw: `raw/Clippings/Claude Cowork + Clay has evolved go-to-market operations.md`. A non-engineer's walkthrough of the [[tool-clay]]-inside-[[tool-claude-code]] (Cowork) integration: two minutes-to-implement use cases. The practical, accessible end of [[concept-data-vs-reasoning-layer]].

## Summary

Two use cases run against a pre-configured Cowork "operating system" that already holds his business context, ICP, positioning and messaging (see his separate "I built a Claude marketing and sales OS" post).

### Use case 1 -- daily outbound prospecting

A single short prompt is enough; Claude asks targeted follow-ups, then surfaces a Clay-enriched contact list cleanly inside the Claude interface. Each contact has its own card (contact info, LinkedIn URL, work-history summary, further enrichment); a company tab exposes hundreds more data points. Claude tiers contacts (Tier 1 / Tier 2 / filter-out) against the stored ICP, then drafts tailored emails into a Gmail drafts folder -- "I would never simply send these; I edit, verify key data points, then send." Minutes end to end.

### Use case 2 -- prioritised, lead-scored list with multiple agents

Started in Clay using Sculptor (voice query: "Find any VP of Sales or CRO at small-to-mid B2B manufacturers in Minneapolis and St. Paul") -> ~30 contacts. Enriched with tech-stack data to filter for HubSpot/Salesforce users (a proxy for an active GTM operation). Exported the table, then had Cowork spin up multiple agents to score and prioritise into three tiers, including checking LinkedIn profiles for AI posts. Only then pulls contact info for chosen contacts and drafts email + LinkedIn connection notes from his positioning. "Hours and days of research compiled in minutes."

## Key takeaways

- The integration's value for non-engineers is presentation plus context: Clay's breadth rendered inside Claude's reasoning, scored against a stored ICP. See [[concept-data-vs-reasoning-layer]].
- Storing business context once (the Cowork OS) is what lets a one-line prompt work -- a lightweight [[framework-gtm-brain]] / [[concept-context-assembly]] in practice.
- A human verify-before-send step on AI-drafted outreach; cf. [[concept-claim-tagging]].
- "Evens the playing field" -- small teams get research-and-campaign capacity that used to need meetings, time, and budget.

## Attribution

[[expert-patrick-schaber]], Approachable AI (patrickschaber.substack.com). References Clay (incl. Sculptor), Claude Cowork, [[tool-granola]], Apollo, Gamma, Descript. Uses Anthropic as a worked (non-target) example.
