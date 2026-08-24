---
title: "Source: Eric Nowoslawski -- Building Clay tables with agents via Browser Use"
type: source
tags: [source, ai-gtm, agentic, automation, tool-integration]
source-title: "How we are building Clay tables with Claude Code and Codex (Browser Use)"
source-url: "https://www.linkedin.com/posts/outboundphd_how-we-are-building-clay-tables-with-claude-activity-7465114556546273280-exe9"
source-author: Eric Nowoslawski
source-published: unknown
raw-path: raw/Eric Nowoslawski/5.md
last-updated: 2026-06-12
last-updated-time: 23:40
---

# Source: Eric Nowoslawski -- Building Clay tables with agents via Browser Use

> LinkedIn post by [[expert-eric-nowoslawski]]. Raw: `raw/Eric Nowoslawski/5.md`.

## Summary

Growth Engine X builds [[tool-clay]] tables with [[tool-claude-code]] and [[tool-codex]], and it works because of how [[tool-browser-use]] does browser automation. Most automation works off screenshots: look at the pixels, guess where to click, hope the layout did not move. Browser Use also reads the front-end API the page uses, so it finds the most dependable way to perform an action rather than pixel-hunting. That is the difference between automation that survives a layout change and automation that silently breaks when a button moves four pixels.

Because of this, they do not maintain files documenting how all of Clay works; the agent learns the UI the way a human would and makes notes when it learns something new. This matters because Clay does not expose a public API, so the browser is the integration surface (commenter Roman Kopytko).

## Key takeaways

- Reading the front-end API beats screenshot/pixel automation for reliability at scale.
- Lets agents operate API-less tools like Clay by learning the interface and taking notes.
- A commenter (Jeremy Ross) claims to have mapped ~90% of Clay's front-end APIs into a "Clay CLI" that never touches the browser, a parallel approach to the same problem.

## Attribution

[[expert-eric-nowoslawski]], Founder Growth Engine X. LinkedIn post.
