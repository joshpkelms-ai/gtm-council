---
title: "Source: Eric Nowoslawski -- Turning AI into full employees (context, connection, creation)"
type: source
tags: [source, ai-gtm, agentic, automation, outbound]
source-title: "Here's the full presentation on how we are turning AI into full blown employees at Growth Engine X"
source-url: "https://www.linkedin.com/posts/outboundphd_heres-the-full-presentation-on-how-we-are-activity-7469818041262981122-p66o"
source-author: Eric Nowoslawski
source-published: unknown
raw-path: raw/Eric Nowoslawski/1.md
last-updated: 2026-06-12
last-updated-time: 23:40
---

# Source: Eric Nowoslawski -- Turning AI into full employees

> LinkedIn post plus presentation transcript by [[expert-eric-nowoslawski]]. Raw: `raw/Eric Nowoslawski/1.md`. The corpus's fullest statement of his "AI as employee" method.

## Summary

Growth Engine X runs outbound on a tiny team by treating coding agents as employees that need training, not instructions. The reframe: if you hired a person and just said "figure it out", they would fail; AI is the same. It costs roughly 3x the effort to train, but once trained it never stops, never takes time off, never leaves.

The three-step framework (see [[framework-ai-employee-loop]]):

1. **Context.** Give the agent access to your system of record (he uses Fathom call recordings and Slack; no heavy CRM) and ask it to build a "company brain" in markdown / Obsidian. Don't over-organise; the million-token window is roughly the length of the Bible, and most companies hold less context than that. Let the model organise itself. Then schedule a daily task to pull new data and update the brain. Compare the lean-brain pushback in the comments (Ivan E.: give agents the 20% that matters, not a folder nobody maintains) and the broader pattern in [[framework-gtm-brain]].
2. **Connection.** Wire up the API keys. His trick: have everyone paste 30 days of Chrome history, de-dupe it with an LLM to list every tool in use, then knock out all the keys in one 15-minute session.
3. **Creation.** Build the loop that makes it an employee. His loop: a scheduled task reads each new Fathom transcript, checks the company brain and relevant skills, drafts an action-item list and a proposed plan; he approves or corrects on his phone; on success it saves feedback (and a skill) for next time.

On security he is explicit that he is not an expert: agents at Growth Engine X run through Trigger.dev, which hides API keys, so he has never handed a raw key to an agent.

## Key takeaways

- The bottleneck is no longer model intelligence but context, connection, and a feedback loop. "If it's not doing what you want, that's your fault."
- Step 3 (proactive plan proposal) is where most people stop short, and it is what turns a tool into a teammate.
- Sub-agents and scheduled tasks let ~7 people outproduce competitors with 30.
- Hide credentials behind a proxy (Trigger.dev) rather than giving keys to agents directly.

## Notable comments

- **Nic Nicolo** distinguishes a memory layer (a repository) from a brain (a feedback loop that changes behaviour from outcomes) -- the live debate behind [[framework-ai-employee-loop]].
- **Ivan E.** argues most teams need a lean, cloud-native "GTM brain" of the 20% that matters (ICP, offers, positioning, references), not a sprawling Obsidian vault. Ties to [[framework-gtm-brain]].

## Attribution

[[expert-eric-nowoslawski]], Founder Growth Engine X. LinkedIn presentation post and transcript.
