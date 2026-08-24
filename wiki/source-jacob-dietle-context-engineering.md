---
title: "Source: Jacob Dietle -- A Context Engineering Deep Dive for GTM"
type: source
tags: [source, ai-gtm, agentic, data, automation, tool-integration]
source-title: "A Context Engineering Deep Dive for GTM with Jacob Dietle, Context Engineer and Founder at Taste Systems"
source-url: "https://thegtmengineer.substack.com/p/a-context-engineering-deep-dive-for"
source-author: "Noah Adelstein (host, the gtm engineer); Jacob Dietle (guest, Taste Systems)"
source-published: 2026-06-01
raw-path: "raw/Clippings/A Context Engineering Deep Dive for GTM with Jacob Dietle, Context Engineer and Founder at Taste Systems 1.md"
last-updated: 2026-06-13
last-updated-time: 11:30
---

# Source: Jacob Dietle -- A Context Engineering Deep Dive for GTM

> A long interview on [[expert-noah-adelstein]]'s the gtm engineer with [[expert-jacob-dietle]], a one-person context-engineering consultancy (Taste Systems). The richest single treatment of [[concept-context-assembly]] in the corpus. Raw: `raw/Clippings/`.

## Summary

Dietle helps companies build a **context OS**: the system that feeds AI the right company context so output jumps from a generic 50-60% to a usable 80-90%. His framing:

- **Context is "information that changes the meaning of other information."** AI is fact-rich but context-poor: it does not know your headcount, your ICP, or how you talk. AI amplifies whatever you give it and otherwise trends to the lowest common denominator.
- **Context ops is a new function**, the GTM analogue of how complex deployment pipelines forced developers to invent DevOps. It needs a "benevolent dictator", a subject-matter expert who owns and maintains the system.
- **Foundation first; find the bottleneck.** Build a small house on a strong foundation, not a sprawling mansion that collapses. Give it all your transcripts but not your ICP and it will make things up. Pick the top three use cases and let them shape how the system evolves.
- **The back-pressure loop.** Start at ~60% (worse than by hand), then iterate: list what is wrong (formatting, missing third-party citations), supply the missing context, regenerate. Software has unit tests as automatic back-pressure; "swishy" GTM work needs you to hand-build it: write three great newsletters, have AI break down what makes them good (tone, sources, structure), and use those building blocks as the test. (He references Toby Lutke's "auto research" as the same loop.)
- **Compounding across use cases.** Solve content once and the same context feeds signals, outbound, and ads ("relevant beats personalised"). Turn a solved process into a skill so the whole team gets it. Ramp is the exemplar: ~700 people using AI daily on a custom company-wide system.
- **Process discovery captures intuition.** Transcribe how you actually do a task: "three steps" is really 27 intuitive micro-decisions. The more expert you are, the more intuitive (and valuable) the capture. The 10-20% AI cannot reach is not a loss; it is your competitive edge, your intuition stamped into the machine (amplification, not replacement). Beware the curse of knowledge: experts forget what they take for granted.
- **Technical setup.** Get into the terminal (intimidating but simple with AI); the force multiplier is read/write to the file system plus running code, plus pushing context in and out of the window so it compounds beyond one session. Use git to version skills and context and to collaborate. "Plain English is now code." Do not chase the cutting edge; find what works for you.

## Buy vs build (the context OS)

Build your own deep workspace ([[tool-claude-code]] / Codex) and also buy an opinionated GTM context tool like [[tool-octave]]. They are complementary:

- **Buy (Octave)** for multiplayer mode and non-technical users: reps and traditional marketers who will not live in Claude Code but need context in their regular AI. Octave ships a solid go-to-market knowledge graph out of the box, with integrations that push to your GTM tools; far less up-front config.
- **Build** for customisation, control of how context flows and self-updates, the long tail of business-specific use cases Octave will not cover, and because understanding the engine makes you better (and makes the bought tool more powerful). Trade-off: customisation gives power but costs setup time.
- Governance for multiplayer: version everything in a GitHub repo; encode the commit/PR cycle as a skill the agent runs; balance "share what is useful and ready" against "commit everything"; PRs let people propose context changes (e.g. a product-marketing module) and test before merging to "prod".

## Key takeaways

- Context = information that changes the meaning of other information; AI amplifies what you give it.
- Foundation before scope; identify the context bottleneck (a missing ICP makes it hallucinate).
- Iterate via back-pressure: decompose a great example into testable building blocks.
- Solve once, turn it into a skill, compound across content/signals/outbound/ads.
- Buy (Octave) for multiplayer and non-technical reach; build for customisation and understanding; do both.

## Attribution

Guest [[expert-jacob-dietle]] (founder, Taste Systems), interviewed by [[expert-noah-adelstein]] on the gtm engineer. Episode sponsored by [[tool-dust]]. See [[concept-context-assembly]], [[framework-gtm-brain]], [[tool-octave]].
