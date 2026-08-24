---
title: "Source: How Vanta's GTM Engineers Used Dust to Turn Every Seller Into an Agent Builder"
type: source
tags: [source, ai-gtm, agentic, automation, tool-integration, enrichment]
source-title: "How Vanta's GTM Engineers used Dust to turn every seller into an agent builder"
source-url: "https://thegtmengineer.substack.com/p/how-vantas-gtm-engineers-used-dust"
source-author: Noah Adelstein
source-published: 2026-05-27
raw-path: "raw/Clippings/How Vanta’s GTM Engineers used Dust to turn every seller into an agent builder.md"
last-updated: 2026-06-13
last-updated-time: 09:00
---

# Source: Vanta's GTM Engineers Used Dust to Turn Every Seller Into an Agent Builder

> GTM Engineer Experiment by [[expert-noah-adelstein]] (the gtm engineer), featuring [[expert-shashank-khanna]] (Head of GTM Engineering, Vanta). Raw: see frontmatter. Anchors [[concept-adoption-as-prioritisation]] and [[play-adoption-driven-roadmap]]; introduces [[tool-dust]]; promotes [[tool-gong]].

## Summary

- **The problem:** of all the workflows that could be built, which are worth the GTM Engineering team's finite hours? Rep ideas can be the most impactful but it is hard to tell up front which will scale.
- **The answer:** democratise agent-building with [[tool-dust]] (no-code, multiplayer, team-oriented; connects to Slack, Drive, Notion, GitHub, Salesforce, Snowflake, with governance controls). Over 900 people at Vanta now use Dust monthly to build agents the whole company can use. Real adoption tells the GTME team which ideas deserve production-grade investment. See [[concept-adoption-as-prioritisation]].
- **How they built it (the play, [[play-adoption-driven-roadmap]]):**
  1. Invested in the data foundation: one source-of-truth fields, no stale data, custom MCPs on top of [[tool-gong]] and Snowflake to gate access and clean garbage ("particularly important with Gong data"), and documented data structure so agents interpret it.
  2. Rolled out company-wide with heavy enablement: vendor sessions, Shashank teaching personally, CRO Stevie Case's weekly all-hands shoutouts to builders, and a post-sales AI PM monitoring usage.
  3. Monitored adoption via Dust admin analytics.
  4. Productionised the winners, ranked by usage: support copilot (most used, now human-managed near full-time), "Cantaloupe 2.0" (merged several account-research/prioritisation/messaging agents into one specialist), competitor monitoring, recruiting copilot.
- **Why Dust uniquely fits:** two layers in one platform -- individual prototyping with shared access (any rep prototypes in an afternoon on gated data) plus central oversight (admin analytics on who builds what and what spreads). If reps could build but the team couldn't see patterns, they'd still be guessing; if the team could see patterns but the builder was too technical or data ungated, too few agents would get built.
- **Three takeaways for replicating it:** use Dust as a discovery layer not just production; invest in the data foundation before opening it to builders (the unglamorous MCP work that made everything possible); build a culture that celebrates builders.

## Key takeaways

- This is the first systematic, bottoms-up way of sourcing GTME use cases -- the discovery-side complement to [[concept-earn-the-right-to-automate]] (whole-org cheap experiments as the proof of demand).
- The data-foundation prerequisite ties straight to [[concept-context-assembly]] (gate and clean upstream) and [[concept-silent-failures]] (garbage data quietly poisons agents).
- "Multiple independently-built agents merged into one" rhymes with [[concept-gtm-functions]] / [[play-clay-function-library]]: collapse duplicated logic into one governed asset.

## Attribution

Author [[expert-noah-adelstein]]. Subject [[expert-shashank-khanna]] (Vanta). Partner/sponsor: Dust. References [[tool-dust]], [[tool-gong]], Snowflake, Salesforce, [[tool-mcp]]; Hearth, Rippling, Netic; The GTM Engineer Lab.

## Related

[[concept-adoption-as-prioritisation]] | [[play-adoption-driven-roadmap]] | [[tool-dust]] | [[tool-gong]] | [[concept-context-assembly]] | [[expert-shashank-khanna]]
