---
title: "Play: Code-first marketing site managed by Claude Code"
type: play
tags: [play, ai-gtm, automation, aeo, tool-integration]
last-updated: 2026-06-13
last-updated-time: 09:00
---

# Play: Code-first marketing site managed by Claude Code

> Rebuild the marketing website off a no-code CMS onto a code-based stack an agent can read and operate, with each recurring web job codified as a [[tool-claude-code]] skill. Lets a one-person team ship pages in hours, bake AEO in by default, and run ABM personalisation without a new vendor. [[expert-rafid-imran]]'s migration of the Yuma AI site. The unlock is treating the site as a [[framework-strategy-as-repo]]-style asset.

## When to use it

Marketing experiment speed is capped by a no-code builder (Webflow, etc.); custom pages, animations, localisation, or AEO infrastructure each turn into mini-projects or paid add-ons.

## Steps

1. **Replicate the existing sitemap.** Ask Claude Code to rebuild the current structure (pages, sections, URL patterns) as a blueprint -- do not port the CMS's quirks.
2. **Choose the stack one capability at a time.** Walk each need (rendering, hosting, styling, content storage, localisation, validation, structured data, interactive components) and let the agent reason through the trade-offs. You do not need the answers, just the right questions. Yuma landed on Next.js (App Router) on Vercel, GitHub, TypeScript end-to-end, Tailwind v4, next-intl, shadcn/ui, MDX for editorial, JSON for structured datasets, Zod for build-time validation, server components by default.
3. **Build core pages from scratch on the new stack.** Homepage, product, pricing, landing-page templates -- faster and cleaner than porting.
4. **Migrate content via the source API.** Pull published blog posts and case studies through the old platform's data API so editorial content stays consistent without dragging in its structure.
5. **Codify every recurring job as a skill.** A skill is a runbook: adding a case study writes the page on the right template, validates metadata, runs the SEO and AEO checks, optimises images, updates internal linking, adds structured data, and ships it -- one prompt instead of a 15-step checklist. See [[concept-skill-namespacing]].

## What it unlocks

- **AEO/GEO by default:** an llms.txt + .md serving layer so ChatGPT, Perplexity, Claude, and AI Overviews can read and cite pages; JSON-LD on every page; server-rendered HTML. See [[concept-aeo]].
- **Revenue-adjacent pages on demand:** ABM pages for target accounts used in ads and outbound, ROI-calculator lead magnets, hyper-targeted industry pages, competitor-displacement comparisons, A/B variants.
- **Localisation in one pass** (translate every page, slug, structured field) with no translation SaaS.
- **Institutional knowledge:** every workflow lives as a skill, so process becomes durable.

The unifying principle: every layer of the stack -- schemas, file conventions, validators, skills -- is readable to the agent the same way it is to a human. A direct instance of [[concept-agent-readiness]].

## Caveats

- Onboarding a freelance writer or agency needs Claude Code plus repo access -- more setup than adding a CMS seat.
- AI costs run high if the agent improvises on every change; plan before building and keep it focused.

## Results (self-reported, Yuma AI, first 30 days)

Users +13%, page views +27%, bounce -21%; recurring cost ~$5,000/year to ~$500/year.

## Related

[[concept-agent-readiness]] | [[concept-aeo]] | [[concept-skill-namespacing]] | [[framework-strategy-as-repo]] | [[tool-claude-code]] | [[tool-framer]]

## Sources

[[source-rafid-imran-code-first-marketing-site]] by [[expert-rafid-imran]].
