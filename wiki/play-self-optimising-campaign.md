---
title: "Play: Self-optimising campaign loop"
type: play
tags: [play, ai-gtm, agentic, campaign-design, outbound, cold-email]
last-updated: 2026-06-12
last-updated-time: 23:40
---

# Play: Self-optimising campaign loop

> Run a weekly optimisation loop over live cold-email campaign data so an agent improves positive-response rate against real outcomes, inside fixed rails. [[expert-eric-nowoslawski]] used this to double a customer's positive lead rate.

## The motion

1. **Gather and lock context first.** Pull all messaging angles, audience targets, and the underlying dataset (built with [[tool-clay]] and Prospeo, stored in Supabase) before the loop runs. Lock the CTA to the real objective so the agent cannot win the wrong way. See [[concept-locked-cta]].
2. **Feed every usable data point upfront.** No game-time decisions: the agent must only ever work from approved inputs, never invent a new way to pull data mid-run.
3. **Run the loop weekly, not every few minutes.** Built on "Autoresearch" (a Karpathy local-ML repo), running over a week's campaign data rather than a tight real-time loop. Across 150+ campaigns in Smartlead, reply and positive-response rates rose two weeks running.

## Why weekly

Outbound feedback is slow and noisy; a weekly cadence over real campaign data gives the loop enough signal to optimise meaningfully, moving from AI generating campaigns to AI improving them.

## Guardrails

- Lock the CTA against reward hacking ([[concept-locked-cta]]); add concrete end-to-end examples of desired behaviour.
- Beware optimising an upstream proxy (sign-ups) without feeding a downstream metric (close rate) back in, or you may pull low-intent volume.

## Source

[[source-eric-nowoslawski-self-optimising-campaign]] by [[expert-eric-nowoslawski]].

## Related

[[concept-locked-cta]] | [[framework-ai-employee-loop]] | [[concept-list-is-the-message]] | [[tool-clay]]
