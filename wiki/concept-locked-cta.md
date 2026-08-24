---
title: "Concept: Locked CTA / no game-time decisions"
type: concept
tags: [concept, ai-gtm, agentic, campaign-design, automation]
last-updated: 2026-06-12
last-updated-time: 23:40
---

# Concept: Locked CTA / no game-time decisions

> When an agent is allowed to optimise a campaign, fix the goal and the inputs before it runs. Lock the call-to-action so it cannot "win" the wrong way, and give it every data point upfront so it never invents an unapproved way to pull data mid-run. [[expert-eric-nowoslawski]]'s guardrail against reward hacking in agentic GTM.

## The two rails

- **Lock the CTA.** If you let an agent optimise for replies or sign-ups without fixing the offer, it can technically "succeed" in ways you never wanted (e.g. giving the product away free to lift sign-ups). Lock the CTA to the real objective (Eric's example: a product sign-up) so every optimisation pulls toward what you actually want.
- **No game-time decisions.** Never let the agent decide mid-run "I want to run an experiment with this data point" and invent a way to fetch it. Feed it every data point it might use upfront so it works only from approved inputs. Eric pre-built the dataset ([[tool-clay]], Prospeo, stored in Supabase) and gathered all messaging and audience context before letting it run.

## Reward hacking

Any eval/optimisation loop can find a path that meets the letter of the goal but not its intent. The mitigation (per Jacob Dietle in the source comments): add concrete end-to-end examples of the desired behaviour so it is hard to fall off the path. A known open risk: optimising to an upstream proxy (sign-ups) can pull low-intent volume unless a downstream metric (close rate) is fed back into the loop.

## Source

[[source-eric-nowoslawski-self-optimising-campaign]] by [[expert-eric-nowoslawski]].

## Related

[[play-self-optimising-campaign]] | [[concept-list-is-the-message]] | [[framework-ai-employee-loop]] | [[concept-claim-tagging]]
