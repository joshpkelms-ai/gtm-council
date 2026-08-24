---
title: "Source: Andy Toizer -- GTM Brain: every campaign makes the next one better"
type: source
tags: [source, ai-gtm, automation, agentic, data, messaging]
source-title: "Claude Code + Codex GTM Context Blueprint"
source-url: https://www.linkedin.com/posts/andy-toizer_claude-code-codex-gtm-context-blueprint-activity-7460380816171249665-U9TY
source-author: Andy Toizer
source-published: unknown
raw-path: raw/Andy Tozier/3.md
last-updated: 2026-06-12
last-updated-time: 23:10
---

# Source: Andy Toizer -- GTM Brain: every campaign makes the next one better

> LinkedIn post plus the GTM Context Blueprint visual (transcribed) by [[expert-andy-toizer]]. Raw: `raw/Andy Tozier/3.md`.

## Summary

Toizer does not want [[tool-claude-code]] to build one good campaign; he wants every campaign to make the next one better. Most teams got the first unlock (use Claude Code or [[tool-codex]] to ship faster: campaign analysis, outbound copy, CRM cleanup, ICP scoring, customer research, sales reports). The next unlock is a loop where agentic work creates company learnings that improve the next output. See [[framework-gtm-brain]].

At Freckle the context was real but scattered: HubSpot (lifecycle, deals, notes, pipeline), ChartMogul (revenue, retention, expansion), PostHog and the database (product usage, workflows), and Fathom/Gmail/Slack/Pylon (buyer language, objections, support pain), plus a human-judgment layer. So he built a "GTM Brain": first inventory source coverage (what is connected, what each tool is for, what is missing, what needs human interpretation before becoming truth), then store the durable version in a repo (company/, icp/, customers/, messaging/, market/, brand/, sales/, systems/).

It clicked when Codex looked across all context and explained what each customer proved about Freckle (e.g. Bolt: PLG signup; ClassDojo: verticalised outbound; Josys: ad audiences). The loop: 1) AI ships the work, 2) the work creates learnings, 3) the learnings improve the next output. Released as a public Claude Code + Codex plugin, GTM Brain Builder.

The visual details 9 agents, including: `source-connector-agent` (routes every GTM fact to its real source), `company-core-agent` (what-we-do, product-truth vs aspirational, approved-claims signed off by legal/leadership), `customer-icp-agent` (ICP, personas, proof-approval), `messaging-market-agent` (positioning, objections, category, competitors), `brand-voice-agent` + `design-system-agent` (voice separate from sales copy; brandkit), `sales-memory-agent` (past campaigns, outbound-copy-guide, emails that got replies), and `freshness-automation-agent` (weekly refresh, source-update-log, proposes updates in Slack for approval).

## Key takeaways

- The compounding loop is the real unlock, not one-off speed. See [[framework-gtm-brain]].
- Route every fact to its owning source; separate product-truth from aspiration; gate "company truth" behind human approval (echoes [[concept-claim-tagging]]).
- Keep voice separate from sales copy; start new outbound from what already replied, not a blank doc.

## Attribution

[[expert-andy-toizer]], Head of Growth at Freckle.io, AgentOperator (agentoperator.substack.com). Original LinkedIn post and GTM Context Blueprint visual.
