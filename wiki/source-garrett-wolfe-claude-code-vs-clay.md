---
title: "Source: Garrett Wolfe -- Can Claude Code Replace Clay? What's hard about AI-GTM"
type: source
tags: [source, ai-gtm, automation, enrichment, tool-integration]
source-title: "Can Claude Code Replace Clay? What's hard about AI-GTM"
source-url: "https://garrettawolfe.substack.com/p/can-claude-code-replace-clay-whats"
source-author: Garrett Wolfe
source-published: 2026-05-19
raw-path: raw/Clippings/Can Claude Code Replace Clay? What's hard about AI-GTM.md
last-updated: 2026-06-12
last-updated-time: 14:30
---

# Source: Garrett Wolfe -- Can Claude Code Replace Clay?

> Substack essay by [[expert-garrett-wolfe]]. Raw: `raw/Clippings/Can Claude Code Replace Clay? What's hard about AI-GTM.md` (a duplicate copy sits in `raw/misc/`; ingested once here). Not a "replace Clay" piece -- "the unvarnished version of what 50 hours in Claude Code looks like, and where my brain keeps reaching for Clay as comparison." The corpus's best failure-mode catalogue for agentic GTM pipelines. Anchors [[concept-silent-failures]].

## Summary

After pre-pitching the "Claude Code for Clay" thesis at Deepline's April Tools Day (having spent under two hours in Claude Code), Wolfe blocked two weeks to actually test it. He built a production pipeline (Deepline + Apollo/Clay -> database -> cron filter/enrich with LeadMagic + Apify -> Deepline/Claude qualify and score 0-100 -> Instantly/LinkedIn routing -> Slack reply bot).

### Gamechangers in Claude Code

- **Speed.** A scoring pipeline that took a week or two to bullet-proof in Clay (4 tables, 80+ columns, stacked merges, custom waterfalls) now takes an hour or two.
- **Code-first, not AI-first.** Title/school/bio string matches become free-forever Python files instead of paid AI tokens. See [[concept-deterministic-first]].
- **A/B testing and rescoring on demand.** "Reweight `senior_eng` to value tenure higher and show me the new top decile" -- done in a sitting.
- **Complex logic.** Index characteristics in Supabase and run DB operations (last-contacted, send-eligibility) beyond Clay's cell-size and logic limits.
- **Use every part of the animal.** No 100-column ceiling: score every data point (all educations, follower count, promotions, bio, headline) for smoother distributions impossible in Clay.

### Where he screwed himself: silent failures

Not Claude-specific -- they'd hit anyone writing pipelines by hand, but a CLI hides nothing the way a spreadsheet UI does. Each was found only by writing an explicit auditor after the fact: a parser wrote 91% of work history to the wrong column (thousands of qualified candidates silently dropped); a contact API returned `200 OK` with empty payloads for private profiles (re-paying for dead URLs); schema drift across six forked copies of a location keyword list leaked the wrong cities; a regex accept-list matched "Staff Engineer" but not "Staff Software Engineer" (6,996 candidates, ~80% of pool, scored zero); macOS silently blocked four days of cron jobs over an iCloud permission grant; a campaign accepted 40 leads on `200 OK` with no senders attached; a managed proxy cost 2x a key he already owned ($1,400+ leak before anyone audited per-row spend).

### Where Claude Code itself is still hard

Open agentic-execution gaps no auditor fixes: inconsistent rate-limit respect (429s mid-run); repeatability (state lives partly in code, partly in conversation -- only code is durable); silent endpoint deprecations (Apollo 404); waterfall design (is vendor-order alpha, or is the vendor stack a commodity?); cursor/pagination state (burned credits on un-resumable runs).

## Key takeaways

- The winner won't be the tool that does more -- it'll be the one that lets a second operator pick up the pipeline without re-discovering every silent failure. The auditability layer is the prize. See [[concept-silent-failures]].
- "Clay is reliable and auditable; Claude is a teammate built for speed." A spreadsheet audit layer on top of an agentic-teammate tool is the generational GTME platform. See [[concept-data-vs-reasoning-layer]].
- Advice to other GTMEs: port one workflow you know cold over a weekend to feel the shape of the tool -- don't migrate the stack.

## Attribution

[[expert-garrett-wolfe]], garrettawolfe.substack.com / OneGTM (getaob.com). References Deepline ([[tool-deepline]]), Clay, Apollo, LeadMagic, Apify, Instantly, Supabase.
