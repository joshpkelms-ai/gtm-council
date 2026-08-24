---
title: "Framework: AI employee loop (context, connection, creation)"
type: framework
tags: [framework, ai-gtm, agentic, automation, outbound]
last-updated: 2026-06-12
last-updated-time: 12:05
---

# Framework: AI employee loop

> [[expert-eric-nowoslawski]]'s method for turning a coding agent into a trainable employee. Solve three things in order -- context, connection, creation -- then close an improvement loop so the agent proposes its own work and learns from your corrections.

## The reframe

Treat AI like a new hire, not a magic box. Handing it instructions and expecting it to "figure it out" is the same mistake that makes a human hire fail. It costs roughly 3x the effort to train, but once trained it never stops, never takes time off, never leaves for a competitor.

## The three steps

1. **Context.** Give the agent access to a system of record (Eric uses Fathom recordings and Slack) and have it build a "company brain" in markdown / Obsidian. Do not over-organise; let the model organise itself within its large context window. Schedule a daily task to pull new data and refresh the brain. This is the same context-repo instinct as [[framework-gtm-brain]] (Toizer) and [[framework-strategy-as-repo]] (Waxman); for the upstream-assembly variant see [[concept-context-assembly]] (Tittarelli).
2. **Connection.** Wire up every API key. Trick: paste 30 days of browser history, de-dupe with an LLM to enumerate every tool in use, then create all keys in one short session. For security, hide keys behind a proxy (Eric uses Trigger.dev) rather than handing them to the agent.
3. **Creation.** Build the loop that makes it an employee.

## The improvement loop

The step most people skip. Eric's loop: a scheduled task detects a new Fathom transcript, reads the company brain and relevant skills, drafts an action-item list and a proposed plan; the human approves or corrects from their phone; on success the agent saves feedback and a reusable skill for next time. Over time it locks in, like a trained employee.

The live debate (from the source comments): is this a memory layer (a repository) or a brain (a feedback loop that changes behaviour from outcomes)? Eric's loop aims at the latter -- learnings change the next run, the compounding idea shared with [[framework-gtm-brain]].

## Why it matters

This is how Growth Engine X runs high-volume outbound on ~7 people: agents respond to leads, clean ICP lists, build TAMs, produce reports, and propose the next campaign. The bottleneck is no longer model intelligence but context, connection, and the loop.

## Source

[[source-eric-nowoslawski-ai-employees-3-step]] by [[expert-eric-nowoslawski]].

The human counterpart of "train the agent like an employee" is [[framework-three-rs-enablement]] (Mercy Bell): apply the same care to developing people that we lavish on agent context and evals.

## Related

[[framework-gtm-brain]] | [[framework-strategy-as-repo]] | [[concept-context-assembly]] | [[play-agentic-goal-run]] | [[concept-deterministic-first]] | [[framework-three-rs-enablement]] | [[tool-codex]] | [[tool-claude-code]]
