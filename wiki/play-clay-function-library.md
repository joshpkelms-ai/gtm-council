---
title: "Play: Build a governed Clay function library"
type: play
tags: [play, enrichment-workflow, automation, tool-integration, revops, governance]
last-updated: 2026-06-12
last-updated-time: 23:55
---

# Play: Build a governed Clay function library

> Convert your most-duplicated GTM workflows into reusable [[tool-clay]] functions, govern them, and expose them to agents. The repeatable motion behind [[concept-gtm-functions]].

## When to run it

When the same enrichment, scoring, or qualification logic is rebuilt across multiple tables; when heavy tables hit column limits; when non-technical teammates need complex workflows without building them; or when the org needs one consistent logic enforced for everyone.

## The motion

1. **Verify, then save.** Confirm a workflow runs correctly, select its columns, right-click "Save as function", and give it a clear name. Never save a function over a broken workflow.
2. **Map inputs and outputs.** Define typed inputs (domain, name, etc.) and the single column(s) returned. Toggle "replace columns with this function" to collapse the raw columns into one clean call.
3. **Start with your top 3-5 duplicated workflows.** Convert the workflows your team rebuilds most often first; let the library grow from there.
4. **Name for a stranger.** Use `workflow type - output - version`, e.g. `contact enrichment - email+phone - V1`. Document each input label clearly -- those labels are the only instructions a future caller gets.
5. **Build governance into the function.**
   - Conditional enrichment: gate expensive steps (phone lookups) behind a checkbox input so callers must opt in.
   - Compliance gating: a region check that halts on restricted geographies (GDPR). Lives inside the function, so it runs for everyone.
   - Reuse before you pay: check for an existing value before running a paid lookup ([[concept-deterministic-first]]).
6. **Keep a credit catalogue.** For 10+ functions, maintain a shared doc/sheet listing each function's inputs, outputs, owner, and cost per row -- per-step cost is hidden from the calling table, so this prevents surprise bills on large batches.
7. **Expose to agents.** Once a function is well-named with structured outputs, call it from Claude, ChatGPT, or Glean over [[tool-mcp]] so reps get account briefs and verified contacts from a chat window without touching Clay.

## Architect vs caller

Split roles deliberately: an ops **architect** builds and maintains the functions; reps, marketers, and SDRs are **callers** who add one column and map inputs. Complexity stays hidden; consistency is enforced.

## Worked examples (from the course)

Firmographic enrichment (3 waterfalls / 12 providers, one column back), corporate-hierarchy mapping (4-phase AI research into a clean family tree), email copywriting (one email in, three send-ready variants out), and job-change detection with backup waterfalls. See [[source-clay-functions-course]] for the builds.

## Sources

[[source-clay-functions-course]] (Clay, presented by Chris Ming).

## Related

[[concept-gtm-functions]] | [[tool-clay]] | [[concept-waterfall-enrichment]] | [[tool-mcp]] | [[play-agentic-prospect-clay-crm-push]] | [[concept-deterministic-first]]
