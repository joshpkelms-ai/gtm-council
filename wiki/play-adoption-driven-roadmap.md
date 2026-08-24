---
title: "Play: Adoption-driven GTM Engineering roadmap"
type: play
tags: [play, ai-gtm, agentic, automation, tool-integration, enablement]
last-updated: 2026-06-13
last-updated-time: 09:00
---

# Play: Adoption-driven GTM Engineering roadmap

> Turn the question "which of infinite workflows do we build?" into a measurement problem. Let the whole org prototype agents on a no-code, governed platform; read real adoption as the roadmap; productionise only the validated winners. Vanta's motion, documented by [[expert-noah-adelstein]] from [[expert-shashank-khanna]]'s work. The principle is [[concept-adoption-as-prioritisation]].

## When to use it

A central GTM Engineering team supports a much larger sales/CS org, has more candidate workflows than hours, and keeps burning time on builds that get no adoption.

## Steps

1. **Build the data foundation first.** One source-of-truth fields (employee size, industry), no stale data, reps given access to clean account data. Build custom MCPs (see [[tool-mcp]]) on top of [[tool-gong]] and Snowflake to gate what reps can reach and to strip garbage. Document how the data is structured so agents interpret it correctly. This is the unglamorous prerequisite -- skip it and agents run on garbage ([[concept-silent-failures]]).
2. **Roll out a multiplayer agent builder org-wide.** Vanta used [[tool-dust]]: no-code, low enough bar that any rep prototypes in an afternoon, with agents shared to the whole org and admin analytics for the central team.
3. **Invest heavily in enablement and a builder culture.** Run sessions with the vendor; the GTME lead teaches many sessions personally; the CRO gives weekly all-hands shoutouts to people who shipped useful agents. Consider a dedicated role (Vanta has a post-sales AI PM) monitoring what resonates.
4. **Monitor adoption, not opinions.** Track which agents are naturally adopted, who builds what, which workflows recur as independently-built variants.
5. **Productionise the winners.** Rebuild the most-adopted workflows as durable systems; merge independently-built duplicates into one specialist (Vanta merged several account-research agents into "Cantaloupe 2.0"). Assign a human owner where usage warrants it.

## Why it works

Dust (or equivalent) is used as a **discovery layer, not just a production system**: its strength is fast prototyping and surfacing genuine demand. Reps are smart and hungry enough to build their own agents; the companies that put building in rep hands find impactful solutions faster than those waiting on leadership or GTME hunches -- and it surfaces ideas the central team would never have thought of.

## Related

[[concept-adoption-as-prioritisation]] | [[tool-dust]] | [[tool-gong]] | [[concept-earn-the-right-to-automate]] | [[play-clay-function-library]] | [[expert-shashank-khanna]]

## Sources

[[source-noah-adelstein-vanta-dust-agent-builders]].
