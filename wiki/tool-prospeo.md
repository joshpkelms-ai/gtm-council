---
title: "Tool: Prospeo"
type: tool
tags: [tool, outbound, enrichment, data, signal-based, campaign-design]
last-updated: 2026-06-12
last-updated-time: 23:40
---

# Tool: Prospeo

> Company and contact data provider used across the corpus for list building and email finding. Its v2 added go-to-market-motion filters that operationalise [[concept-list-is-the-message]].

## What it is

A B2B data tool for sourcing companies and contacts (and finding/verifying emails). Appears repeatedly as an enrichment source, often inside a waterfall alongside other providers (e.g. BlitzAPI, Parallel Web Systems Entity search) under [[concept-waterfall-enrichment]], and as a dataset source for campaigns.

## What v2 added

- **Who they sell to** -- filter companies by the audience they sell into (small-business owners, legal, marketing), the size of those customers, and the market. This is the segmentation axis behind [[concept-list-is-the-message]].
- **Full-site keyword search** across page bodies, titles, URLs, and SEO descriptions (not just company description); big recall lift.
- **Business-model / type filters** -- SaaS, marketplace, e-comm, agency, consulting, manufacturing, plus flags like "public pricing page", "enterprise plan", "usage-based pricing".
- **AI attributes** -- offers a demo, has an API, has a blog.
- **Google Discovery** -- find companies by who ranks for a keyword.
- All exposed in the API, not just the UI.

## Position in the corpus

[[expert-eric-nowoslawski]] requested several of these filters and rates them as a fast starting point unmatched elsewhere, with the caveat that for a complete TAM exactly to spec you still pull the broad list and finish it with your own deterministic website checks ([[concept-deterministic-first]]).

## Sources

[[source-eric-nowoslawski-prospeo-sell-to-targeting]], [[source-eric-nowoslawski-list-is-the-message]], [[source-eric-nowoslawski-goal-mode-10-tasks]].

## Related

[[concept-list-is-the-message]] | [[concept-waterfall-enrichment]] | [[concept-deterministic-first]] | [[tool-clay]]
