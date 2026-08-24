---
title: Garrett Wolfe
type: expert
tags: [expert, ai-gtm, automation, enrichment, tool-integration]
author: Garrett Wolfe
last-updated: 2026-06-12
last-updated-time: 14:30
---

# Garrett Wolfe

> GTM engineer building bespoke outbound infrastructure (for Coastal, with David, Asher, and Kyle) and writing at garrettawolfe.substack.com; also behind OneGTM (getaob.com). Spoke at Deepline's April Tools Day on bespoke sales tooling, then ran a two-week, 50-hour experiment porting his GTM stack into [[tool-claude-code]]. His honest field report is the corpus's sharpest account of what breaks when you move from a spreadsheet UI to a CLI.

## Who he is

A practising GTME and Clay power user ("most of my mental model for what a modern GTM workflow even looks like was shaped by Clay"). Frames Claude Code as Clay's natural reference point, not its antagonist. Notes the Clay pricing change created "a permission structure" for operators to test the other side.

## Core positions

- **Code-first, not AI-first.** Much of what people spend AI tokens on is deterministic code in disguise -- string matches, keyword checks -- that becomes a Python file running free forever once written. The per-row cost difference is meaningful across hundreds of thousands of rows. Same discipline as [[concept-deterministic-first]].
- **Escape the column ceiling.** A spreadsheet caps at ~80-100 columns; he only ever used 10-15 data points. In code he can score every data point (all educations, follower count, promotion count, bio, headline) for far smoother score distributions. This is the mechanical case behind [[concept-list-is-the-message]] and richer scoring.
- **Clay is auditable, Claude is a fast teammate.** A spreadsheet is auditable by default (every column is visible logic); a teammate is fast and inventive but opaque, living "partly in code and partly in conversation". See [[concept-data-vs-reasoning-layer]].
- **Whoever wins builds the auditability layer.** The generational GTME platform puts a spreadsheet-shaped audit layer on top of an agentic-teammate-shaped tool. Anchors [[concept-silent-failures]].

## What he built

A production pipeline: Deepline + Apollo/Clay webhook title-matched leads into a database; a cron job filters and enriches (LeadMagic, Apify); Deepline/Claude qualifies and scores 0-100 by persona; high scores route to Instantly, top scores to LinkedIn; replies pipe to Slack and are answered by a custom AI bot from Slack. Recurring drip plus targeted campaigns. Honest caveat: most GTME work like this is still one-offs and tests, rarely in production at scale.

## Sources

- [[source-garrett-wolfe-claude-code-vs-clay]] -- 50 hours in Claude Code; the gamechangers, the silent failures, the open agentic-execution gaps.

## Related

[[concept-silent-failures]] | [[concept-data-vs-reasoning-layer]] | [[concept-deterministic-first]] | [[tool-claude-code]] | [[tool-deepline]] | [[tool-clay]]
