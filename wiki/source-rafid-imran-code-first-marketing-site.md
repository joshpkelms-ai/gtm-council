---
title: "Source: How One Person Ships Marketing Pages 12x Faster After Ditching Webflow"
type: source
tags: [source, ai-gtm, automation, aeo, tool-integration]
source-title: "How One Person Ships Marketing Pages 12x Faster After Ditching Webflow"
source-url: "https://thegtmengineer.substack.com/p/how-one-person-ships-marketing-pages"
source-author: Rafid Imran
source-published: 2026-06-02
raw-path: "raw/Clippings/How One Person Ships Marketing Pages 12x Faster After Ditching Webflow.md"
last-updated: 2026-06-13
last-updated-time: 09:00
---

# Source: One Person Ships Marketing Pages 12x Faster After Ditching Webflow

> First-person account by [[expert-rafid-imran]] (growth, Yuma AI), published on [[expert-noah-adelstein]]'s the gtm engineer. Raw: see frontmatter. Anchors [[play-code-first-marketing-site]]; feeds [[concept-agent-readiness]], [[concept-aeo]], [[concept-skill-namespacing]].

## Summary

- **The move:** migrated Yuma AI's entire marketing site off Webflow onto a code-based stack managed almost entirely through [[tool-claude-code]]. One person, no agency or dev team, now doing the work of five and shipping pages twice a week.
- **Why leave Webflow:** custom work became mini-projects; animations and high-function pages were painful; templates and CMS forced content into rigid shapes; recurring platform + Weglot translation cost; the core problem was that marketing experiment speed was capped by the tool.
- **The migration:** ~1.5 weeks with the eng team's help. Rebuilt from scratch the way they wanted rather than porting Webflow's structure, then synced published content over via the Webflow Data API.
- **The biggest unlock -- Claude skills as runbooks.** A skill codifies a recurring web job (add a case study, spin up a comparison page, SEO preflight, slug change with redirects). Adding a case study now writes the page on the right template, validates metadata, runs SEO/AEO checks, optimises images, updates internal linking, adds structured data, and ships -- one prompt vs a 15-step checklist. Better than a template because a template is only a visual starting point; a skill does everything around it. Ties to [[concept-skill-namespacing]] and [[framework-strategy-as-repo]].
- **AEO/GEO baked in:** /llms.txt and .md endpoints for ChatGPT, Perplexity, Claude, and AI Overviews to read and cite; JSON-LD on every page; server components by default so crawlers see real HTML. See [[concept-aeo]].
- **Other unlocks:** ABM pages for target accounts (ads + outbound), ROI-calculator lead magnets, hyper-targeted industry pages, competitor-displacement comparisons, A/B variants; one-pass localisation with no Weglot; automated content-aware internal linking; build-time Zod validation; far better Core Web Vitals.
- **The stack (chosen one capability at a time, with Claude reasoning the trade-offs):** Next.js (App Router) on Vercel, GitHub, TypeScript, Tailwind v4, next-intl, shadcn/ui, MDX, JSON datasets, Zod, server components. Unifying theme: every layer is readable to the agent the same way it is to a human -- a direct instance of [[concept-agent-readiness]].
- **Caveats:** onboarding writers/agencies needs Claude Code + repo access (more than a CMS seat); AI costs run high if the agent improvises -- plan first, keep it focused.
- **Results (self-reported), first 30 days:** users +13%, page views +27%, bounce -21%; recurring cost ~$5,000/year (Webflow + Weglot) to ~$500/year (Vercel Pro).

## Key takeaways

- The marketing site becomes a [[framework-strategy-as-repo]]-style asset: version-controlled, agent-operable, with process captured as skills (institutional knowledge).
- A demand-side and mechanics-side pairing with [[concept-aeo]]: the AEO infrastructure here is the concrete build behind the principle.
- Strong corroboration of [[concept-agent-readiness]] (Toizer): design the artefact so the agent can operate it directly.

## Attribution

Author [[expert-rafid-imran]] (Yuma AI), published by [[expert-noah-adelstein]] (the gtm engineer). References Webflow (and its Data API), Weglot, [[tool-claude-code]], Next.js, Vercel, GitHub, TypeScript, Tailwind, next-intl, shadcn/ui, MDX, Zod.

## Related

[[play-code-first-marketing-site]] | [[concept-agent-readiness]] | [[concept-aeo]] | [[concept-skill-namespacing]] | [[framework-strategy-as-repo]] | [[tool-claude-code]]
