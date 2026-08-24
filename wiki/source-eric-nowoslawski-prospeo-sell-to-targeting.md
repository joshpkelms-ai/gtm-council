---
title: "Source: Eric Nowoslawski -- Target companies by who they sell to (Prospeo update)"
type: source
tags: [source, outbound, enrichment, data, signal-based, campaign-design]
source-title: "You can now target companies by who they sell to (Prospeo update)"
source-url: "https://www.linkedin.com/posts/outboundphd_you-can-now-target-companies-by-who-they-activity-7462849710442217472-rpcG"
source-author: Eric Nowoslawski
source-published: unknown
raw-path: raw/Eric Nowoslawski/8.md
last-updated: 2026-06-12
last-updated-time: 23:40
---

# Source: Eric Nowoslawski -- Target companies by who they sell to

> LinkedIn post by [[expert-eric-nowoslawski]]. Raw: `raw/Eric Nowoslawski/8.md`. Companion to [[source-eric-nowoslawski-list-is-the-message]].

## Summary

A walkthrough of [[tool-prospeo]]'s v2 filters, several of which Eric requested. The new axes:

- **Who they sell to**: companies that sell to small-business owners, legal teams, marketing, etc., plus the size of the companies they sell to and the market they are in. This is the segmentation axis behind [[concept-list-is-the-message]].
- **Full-site keyword search**: reads page bodies, titles, URLs, and SEO descriptions, not just the company description; big lift in recall.
- **Business-model and type filters**: SaaS, marketplace, e-comm, agency, consulting, manufacturing, plus flags like "has a public pricing page", "has an enterprise plan", "usage-based pricing".
- **AI attributes**: offers a demo, has an API, has a blog.
- **Google Discovery**: find companies by who ranks for a given keyword.
- All of it is in the API, not just the UI.

Honest read on data quality: great for a quick, well-defined list; for a complete TAM exactly to spec, still pull the broad list and finish it with your own website prompts. As a fast starting point he has not seen filters like this elsewhere.

## Key takeaways

- "Who they sell to" replaces revenue bands as a stand-in for go-to-market motion (commenter Yannic Schwock).
- Propensity flags like "has a public pricing page" / "usage-based pricing" save bespoke scraping (commenter Christian Sorensen).
- Use as a fast start, not a source of truth for full-spec TAMs; finish with your own deterministic website checks. Connects to [[concept-deterministic-first]].

## Attribution

[[expert-eric-nowoslawski]], Founder Growth Engine X. LinkedIn post with video walkthrough.
