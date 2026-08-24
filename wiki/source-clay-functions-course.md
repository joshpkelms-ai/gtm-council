---
title: "Source: Clay -- Functions course (8 lessons)"
type: source
tags: [source, enrichment, automation, enrichment-workflow, tool-integration, ai-gtm]
source-title: "Clay Functions (course)"
source-url: "https://university.clay.com/lessons/introduction-to-functions"
source-author: Clay (presented by Chris Ming)
source-published: 2026-04-14
raw-path: raw/Clippings/ (lessons 1-6, 8 transcripts; written variants "... Functions.md")
last-updated: 2026-06-12
last-updated-time: 23:55
---

# Source: Clay -- Functions course (8 lessons)

> Clay's official course teaching its Functions feature, presented by Chris Ming. Held in `raw/Clippings/` in two formats: YouTube transcripts (`1 Introduction to Functions...` through `8 What's Possible Next...`) and the written university.clay.com lessons (`Introduction to Functions Functions.md` etc.). Same content, two formats; distilled here as one body. Documents the [[tool-clay]] Functions feature and the [[concept-gtm-functions]] principle.

## The course

Eight lessons (lesson 7 is "Use Case: Signal Detection & Lead Qualification"; there is no standalone numbered "7" transcript file, only the written variant):

1. **Introduction to Functions: Build Once & Apply Everywhere** -- what a function is and why it beats templates.
2. **Build Your First Function** -- save a tested waterfall as a function, map inputs/outputs, call it elsewhere, edit once and propagate.
3. **Roll Functions Out Across Your Team** -- workspace-level library; architect vs caller; governance patterns.
4. **Scale and Maintain Your Function Library** -- naming system, credit visibility catalogue, scaling past limits.
5. **Use Case: Contact & Account Enrichment** -- firmographic enrichment and corporate-hierarchy mapping functions.
6. **Use Case: Email Copywriting** -- one email address in, three ready-to-send variants out.
7. **Use Case: Signal Detection & Lead Qualification** -- job-change detection at scale with backup waterfalls.
8. **What's Possible Next: Functions Beyond the Table** -- functions called from outside Clay via MCP.

## What a Function is

A reusable workflow built from any set of columns in Clay. Define it once, set inputs (domain, name, etc.), define outputs, and save. Anyone in the workspace can then call it into any table. The function does not run inside your table: it spins up a hidden "mini table" in the background, does all the work there, and pipes a single column back. Your main table stays clean, returning one column instead of fifteen.

The framing metaphor: a recipe in a restaurant kitchen. The head chef writes it once; every line cook follows it; change mangoes to papayas and every cook changes too.

## Functions vs templates (the core argument)

Templates are copy-paste: once pasted into a new table the copy is its own thing, so updating logic means hunting through every table manually (the lesson's example: a lead-scoring workflow copied across 20 tables, ICP shifts, you must edit all 20 and still miss some). Functions are **call, not copy**: one version of the logic lives in one place, and editing it in the Function Library auto-propagates to every table that calls it. This is [[concept-gtm-functions]] -- a single source of truth for GTM logic; see also [[concept-borrow-from-engineering]] (it is DRY / functions-as-code applied to GTM).

Four signals you should turn a workflow into a function:
1. The same enrichment logic runs across more than one table.
2. You are hitting column limits on a heavy enrichment table.
3. You want non-technical teammates to run complex workflows without building them.
4. Governance: every team must use the same qualification and enrichment logic (no SDR / AE / partnership team scoring three different ways).

## Team rollout and governance (lesson 3)

Functions live at the workspace level: shared infrastructure, not private knowledge buried in one person's table. The ops person becomes the **architect**; reps, marketers, SDRs become **callers** who add one column, map inputs, and get structured data back without knowing the waterfall underneath. Onboarding collapses to "point them at the library".

Two governance patterns to build in from the start:
- **Conditional enrichment** -- gate expensive steps (e.g. phone lookups) behind a checkbox input so a caller must explicitly opt in; stops accidental credit burn on thousands of rows.
- **Compliance gating** -- a conditional step checks a contact's region before enrichment and halts on restricted geographies (e.g. GDPR). Because the check lives inside the function, it runs for every caller and nobody can skip it.

## Scale and maintenance (lesson 4)

- **Naming system:** workflow type -> output -> version, e.g. `contact enrichment - email+phone - V1`. Makes alphabetical sorting in the library actually useful (all contact functions group together). Avoid `enrichment v2 final final`.
- **Credit visibility:** for 10+ functions keep a simple internal catalogue (doc or sheet) listing each function's inputs, outputs, owner, and **cost per row**. Critical because per-step credit cost shows on the function view, not the calling table, so a caller running a 4-credit function across 10,000 rows gets a surprise bill.
- **Scaling past limits:** logic lives in the background mini table, so it never counts against the main table's column limit; and functions removed the old 50,000-row cap via pass-through, so they run on unlimited rows.

## Worked functions (lessons 5-7)

- **Company firmographic enrichment** -- inputs: domain, name, LinkedIn URL, CPJ employee count. Three parallel waterfalls (revenue: HG Insights, People Data Labs, Pubrio, RocketReach; employee count: reuses CPJ count first, then the four providers, then Clearbit and SMARTe; web traffic: Semrush, SerpStat, Datagma, Store Leads). 12 provider lookups, one column back. Reuses an existing employee count before paying for a fresh lookup ([[concept-deterministic-first]] in spirit). Built on [[concept-waterfall-enrichment]].
- **Corporate hierarchy mapping** -- inputs: domain, location, name. Four phases: (1) deep research (company overview AI agent, address-footprint agent, EMEA/HG pre-existing hierarchy pull via HitHorizons + HG Insights); (2) intelligence synthesis (hierarchy scrape agent over filings/press/about pages, plus a gap-fill agent); (3) consolidation that resolves conflicts between sources into a clean family tree (immediate vs ultimate parent); (4) extract parent/subsidiary fields and send back. Solves the "is this Starbucks the corporation or a franchise" problem.
- **Email copywriting** -- input: one contact email. Pulls the Salesforce contact + account ID, then two Snowflake queries (person-level: product usage, call transcripts, job changes; account-level: firmographics, account-wide conversation data). [[tool-claude-code|Claude]] runs persona/seniority analysis and writes a 4-6 sentence SDR cheat-sheet, then outputs three variants -- insights-led (insight + soft CTA), value nugget (tactical tip), high signal (top qualifying signal, returns "no high signal" if none). Writes all three back as JSON for the SDR (or an agent) to choose and route to Slack or a sequencer.
- **Job-change detection (signal/qualification)** -- inputs: full name, first, last, account name. Enriches LinkedIn, an AI step decides if the person still works at the target company and their current role/relationship. Backup waterfalls if the LinkedIn lookup fails: domain (Claygent, HG Insights, Google), work email (11 providers: LeadMagic, Findymail, Prospeo, Dropcontact, Hunter, Datagma, Wiza, PDL, Enrow, FullEnrich, BetterContact), and reverse LinkedIn-from-email (12 methods). Teams run large fleets of signal agents as functions.

## Functions beyond the table (lesson 8)

The strategic point: Clay Functions can be **called from outside Clay** -- from Claude, ChatGPT, Glean and others -- via [[tool-mcp]] integrations. A rep types a company into a chat window and gets back a full account brief or a verified contact; they never see the function. Every function is therefore potentially callable by another tool, which makes naming, input definitions, and output structure matter beyond your own use. Functions are positioned as the infrastructure layer powering the whole GTM stack whether or not the end user ever opens a Clay table. This is the same rep-facing MCP stance Patrick Spychalski describes in [[source-patrick-spychalski-clay-mcp]].

## Key takeaways

- A function is a single source of truth for one piece of GTM logic: call not copy, edit once, propagate everywhere. See [[concept-gtm-functions]].
- The architect/caller split is the org win: complexity hidden behind one column, governance and compliance enforced for everyone who calls.
- Governance is built into the function (conditional gating, compliance checks, credit catalogue), not policed manually.
- Functions are MCP-exposable, making them the connective tissue between Clay and agentic front-ends. See [[play-clay-function-library]].

## Attribution

Clay (the company); course presented by Chris Ming, with Jake (head of studio) credited. Available on all paid Clay plans at no extra cost. Raw transcripts and written lessons in `raw/Clippings/`.
