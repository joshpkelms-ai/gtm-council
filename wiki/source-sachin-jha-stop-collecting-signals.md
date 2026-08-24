---
title: "Source: Sachin Jha -- Stop Collecting Signals Like Pokemon Cards"
type: source
tags: [source, signal-based, data, outbound, messaging]
source-title: "Stop Collecting Signals Like Pokemon Cards"
source-url: "https://sachcode.substack.com/p/stop-collecting-signals-like-pokemon"
source-author: Sachin Jha
source-published: 2026-02-19
raw-path: raw/Clippings/Stop Collecting Signals Like Pokemon Cards.md
last-updated: 2026-06-12
last-updated-time: 12:00
---

# Source: Sachin Jha -- Stop Collecting Signals Like Pokemon Cards

> Substack essay by [[expert-sachin-jha]], drawn from ONEGTMLab podcast Episode 1 with Piyush Agarwal (co-founder, Reo.Dev). Raw: `raw/Clippings/Stop Collecting Signals Like Pokemon Cards.md`. Introduces the [[framework-signal-intelligence-layer]] and the [[concept-signal-vs-intent]] distinction.

## Summary

GTM teams collect signals like Pokemon cards: lots of data, very little action. The core confusions and claims:

- **Intent data is not signal.** Intent says who *might* be interested; signal says who is *already moving* and *why*, with a short window. Nobody downloads a whitepaper to get an SDR call; the real signal is "struggling with their Kubernetes deployment this week". Approach after the window and the opportunity is gone (two months early = no response; two months late = already chose). See [[concept-signal-vs-intent]].
- **A once-in-a-decade shift.** CRM was paper 30 years ago, Salesforce moved it to the cloud 20 years ago, HubSpot mainstreamed inbound 10 years ago. Now the signals teams built their playbook on are decaying: half of website visitors are bots/agents; searches move from Google to ChatGPT. Running GTM on Bombora + visitor tracking alone is decaying infrastructure.
- **Signal hoarding is the real problem.** Teams have Common Room, six enrichment tools, job-change/funding/tech-stack/competitor alerts, beautiful dashboards, and then no workflow connecting signal to the next conversation. Signal should change *how* you show up, not just *who* you target (a FedRAMP cycle or a Kubernetes cost problem changes your opening line and your questions).

## The Signal Intelligence Layer

Three tiers; match motion to tier. See [[framework-signal-intelligence-layer]]. Layer 1 early intent (high-volume, low-intent: social engagement, scroll depth, community questions) is narrative territory, not outbound. Layer 2 mid intent (pricing-page views, buying-context LinkedIn posts, stack changes, competitor ad exposure) is in-market. Layer 3 high intent (demo-page visits, integration docs, funding, sales-leader hires, migration indicators) is act-fast, and where teams drop the ball as the window closes.

## DevTools is a different animal

Developers try products from an IDE plugin, Docker image, GitHub Action, anonymous sign-up -- no form fill, no CRM entry (Reo found customers like SpaceX they had no idea were users). Traditional intent data breaks; you need behavioural signals (installs, deployments, doc engagement, open-source activity). The same signal means different things to different companies (a hiring signal differs for Confluent vs a code-security tool); making the signal-to-implication leap is the GTM engineer's brain, "not automatable yet".

## Foundations and the future

Fix product-marketing foundation before stacking tools: clear ICP, message-market fit, channel-market fit. Bring in signal tooling after PMF, then use it to "find more people with the same pain". Future: a GTM intelligence layer sits *before* the CRM, machines prioritise/route, humans own strategy and creative. Tools level up the 90% who aren't already top-decile researchers. "Software to see, humans to act." Open-sourced assets: a Figma "GTM Signal Intelligence Layer" file and an "Intent Signals Scoring Sheet".

## Key takeaways

- The intent/signal distinction is the most-cited idea here; pairs with [[framework-signal-intelligence-layer]].
- Connects to [[concept-list-is-the-message]] (the data point changes the message) and to the foundation-first sequencing of [[framework-three-layer-gtm]].

## Attribution

[[expert-sachin-jha]] (ONEGTMLab), with Piyush Agarwal (Reo.Dev) on the ONEGTMLab podcast, hosted by Shruti Verma. Substack.
