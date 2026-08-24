---
title: "Framework: GTM Brain (compounding GTM context)"
type: framework
tags: [framework, ai-gtm, automation, agentic, data, messaging]
last-updated: 2026-06-13
last-updated-time: 11:30
---

# Framework: GTM Brain

> [[expert-andy-toizer]]'s system for turning scattered GTM context into an agent-ready repo that compounds: AI ships the work, the work creates learnings, the learnings improve the next output. Released as the GTM Brain Builder plugin (Claude Code + Codex).

## The loop

The point is not to build one good campaign but to make every campaign improve the next:

1. **AI ships the work** (campaign analysis, outbound copy, CRM cleanup, ICP scoring, customer research, sales reports).
2. **The work creates learnings** (which audience + offer + channel actually drives pipeline; which fields are reliable; which workflow language lands).
3. **The learnings improve the next output.**

Better context creates better outputs. This is the compounding cousin of [[framework-strategy-as-repo]].

## The build

1. **Source coverage first.** Inventory the connected stack: what each tool is for, what is missing, and what needs human interpretation before it becomes "company truth". Route every fact to its owning source (e.g. ChartMogul owns revenue, [[tool-hubspot]] owns CRM, PostHog owns usage).
2. **Store the durable version in a repo**, organised by domain: `company/`, `icp/`, `customers/`, `messaging/`, `market/`, `brand/`, `sales/`, `systems/` (and `automation/`).

## The 9 agents (GTM Brain Builder)

- `source-connector-agent` -- inventories the stack; `sources.md`, `tools.md`, `source-coverage.md`.
- `company-core-agent` -- `what-we-do.md`, `product-truth.md` (shipped vs aspirational), `approved-claims.md` (signed off, sourced).
- `customer-icp-agent` -- `our-icp.md`, `personas.md`, `proof-approval.md` (which customer tells which story).
- `messaging-market-agent` -- `positioning.md`, `objections.md`, `category.md`, `competitors.md`.
- `brand-voice-agent` + `design-system-agent` -- voice profiles and tone (kept separate from sales copy); brandkit and design rules.
- `sales-memory-agent` -- `campaigns.md`, `outbound-copy-guide.md`, `email-examples.md` (cold emails that got replies).
- `freshness-automation-agent` -- weekly refresh, `source-update-log.md`, proposes updates in Slack; `mvp-checklist.md` keeps the build in scope.

## Discipline

Nothing is promoted to "company truth" silently. Product-truth is separated from aspiration; approved-claims are signed off; weekly refreshes propose updates for human approval. Mirrors [[concept-claim-tagging]].

Three rules from the build diary ([[source-andy-toizer-company-memory-layer]]):

- **Evidence vs meaning.** "Tools provide evidence. Operators provide meaning. The GTM Brain stores the version future agents should use." Same split as [[concept-context-assembly]]'s data-layer-vs-human-judgment line.
- **Grill Me, do not approve.** Have the agent interrogate the operator (one pointed question, current best hypothesis, why it matters, what changes by the answer) rather than rubber-stamp a long plan. Uses the Grill Me skill (Matt Pocock).
- **Language steers the agent.** Call it "strategy" and it improvises strategy; call it "context" and it preserves what is already true. Scrub "strategy" to "durable context", "working theory", "source-backed evidence", or "accountable-owner review". An MVP checklist stops drift toward building campaigns instead of the brain.

## Sources

[[source-andy-toizer-gtm-brain]] (LinkedIn launch) and [[source-andy-toizer-company-memory-layer]] (full AgentOperator build diary), both by [[expert-andy-toizer]].

## Related

[[framework-strategy-as-repo]] | [[concept-claim-tagging]] | [[concept-context-assembly]] | [[tool-claude-code]] | [[tool-codex]] | [[tool-hubspot]] | [[tool-agent-skills]] | [[concept-borrow-from-engineering]] | [[expert-jacob-dietle]]
