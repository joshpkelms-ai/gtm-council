---
title: "Source: Eric Nowoslawski -- A fully AI-managed campaign built on Autoresearch"
type: source
tags: [source, ai-gtm, agentic, outbound, campaign-design, cold-email]
source-title: "We launched a fully AI managed campaign for a customer using Autoresearch as the foundation"
source-url: "https://www.linkedin.com/posts/outboundphd_we-launched-a-fully-ai-managed-campaign-for-activity-7467595535072276483-2NmD"
source-author: Eric Nowoslawski
source-published: unknown
raw-path: raw/Eric Nowoslawski/3.md
last-updated: 2026-06-12
last-updated-time: 23:40
---

# Source: Eric Nowoslawski -- A fully AI-managed campaign built on Autoresearch

> LinkedIn post by [[expert-eric-nowoslawski]]. Raw: `raw/Eric Nowoslawski/3.md`.

## Summary

Eric ran a fully AI-managed cold-email campaign that doubled a customer's positive lead rate. The foundation was "Autoresearch", which he attributes to "Andre Kapathi" (Andrej Karpathy) as a GitHub repo for running local machine learning easily. Instead of a tight 5-minute optimisation loop, he ran it weekly over real cold-email campaign data to push positive response rates up. See [[play-self-optimising-campaign]].

The setup discipline is the lesson:

- **Lock the CTA before optimising.** The goal was a product sign-up; if the CTA were open, the agent could "win" by giving the software away free. See [[concept-locked-cta]].
- **No game-time decisions.** Feed the agent every data point it might use upfront so it never invents an unapproved way to pull data mid-run. They gathered all messaging context, audience targets, and the dataset (built with [[tool-clay]] and Prospeo, stored in Supabase) before letting it run.
- **Let it optimise within the rails.** Running 150+ campaigns in Smartlead, it raised reply and positive-response rates two weeks running, always pulling toward the locked sign-up CTA.

## Key takeaways

- Move from AI generating campaigns to AI improving campaigns against real performance data; that is where compounding starts (commenter Oleg Pavlovski).
- Watch reward hacking: an eval loop can "succeed" in ways you did not intend. Jacob Dietle recommends adding concrete end-to-end examples so it is hard to fall off the path.
- Open question raised by commenter Leo Bosuener: sign-up is upstream of revenue; an agent optimising to sign-ups may pull low-intent ones unless close rate is fed back into the loop.

## Attribution

[[expert-eric-nowoslawski]], Founder Growth Engine X. LinkedIn post. "Autoresearch" attributed in-post to Andrej Karpathy (spelling per source: "Andre Kapathi").
