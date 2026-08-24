---
title: "Concept: GTM functions (call, not copy)"
type: concept
tags: [concept, automation, enrichment-workflow, tool-integration, revops, ai-gtm]
last-updated: 2026-06-12
last-updated-time: 23:55
---

# Concept: GTM functions (call, not copy)

> Package a GTM workflow once as a callable function with defined inputs and outputs, so one version of the logic lives in one place and updates propagate to every table or tool that calls it. The DRY principle of software engineering applied to enrichment and qualification logic. Named and shipped as a feature in [[tool-clay]]; the principle generalises.

## The principle

Most GTM teams duplicate logic: the same enrichment waterfall, lead-scoring model, or qualification rule copied across many tables. Copies drift. When the ICP shifts or a provider changes, someone must hunt down every copy and edit it by hand, and will miss some.

A function inverts this. You define the logic once, expose it as a named function with typed inputs and outputs, and everywhere else **calls** it rather than copying it. Edit the function in one place and every caller gets the new version automatically. This is the engineering idea of a function / single source of truth, ported to GTM. See [[concept-borrow-from-engineering]].

## Why it matters

- **Consistency / governance.** One qualification logic for the whole org -- no SDR, AE, and partnership team scoring the same lead three different ways. Compliance and credit gates built into the function run for every caller and cannot be skipped.
- **Abstraction.** An ops "architect" builds the function; non-technical "callers" add one column and get clean structured data back without understanding the waterfall underneath. Onboarding collapses to pointing people at a library.
- **Cleanliness and scale.** Logic runs in a hidden background table, so it never consumes the calling table's column budget, and (in Clay) lifts the row cap via pass-through.

## Relationship to other ideas

- It is the natural home for a [[concept-waterfall-enrichment]]: build the waterfall once, expose it as a function, call it everywhere.
- Reusing a value you already hold before paying to re-fetch it (e.g. checking an existing employee count before running the lookup) is [[concept-deterministic-first]] inside a function.
- A function with built-in compliance and consistency rules is a close cousin of the "trusted write layer" idea -- governed logic an agent can call but not subvert; compare the locked rails of [[concept-locked-cta]].

## The agentic turn

Functions become powerful once they are callable from outside their host tool. Clay exposes functions over [[tool-mcp]] so they can be invoked from Claude, ChatGPT, or Glean: a rep types a company into a chat window and gets a full account brief, never seeing the function. This is the same rep-facing MCP stance in [[source-patrick-spychalski-clay-mcp]], and the motion is captured in [[play-clay-function-library]].

## Sources

[[source-clay-functions-course]] (Clay, presented by Chris Ming).

## Related

[[tool-clay]] | [[concept-waterfall-enrichment]] | [[concept-borrow-from-engineering]] | [[concept-deterministic-first]] | [[tool-mcp]] | [[play-clay-function-library]]
