---
title: "Source: Agent Skills documentation (agentskills.io)"
type: source
tags: [source, reference, ai-gtm, agentic, automation]
source-title: "Agent Skills: Overview, Specification, Best practices, Optimizing descriptions"
source-url: "https://agentskills.io/home | https://agentskills.io/specification | https://agentskills.io/skill-creation/best-practices | https://agentskills.io/skill-creation/optimizing-descriptions"
source-author: agentskills.io (Anthropic ecosystem)
source-published: unknown
raw-path: "raw/Clippings/Agent Skills Overview.md, raw/Clippings/Specification.md, raw/Clippings/Best practices for skill creators.md (and duplicate '... 1.md'), raw/Clippings/Optimizing skill descriptions.md"
last-updated: 2026-06-13
last-updated-time: 10:30
---

# Source: Agent Skills documentation (agentskills.io)

> The official reference set for the Agent Skills format, distilled into [[tool-agent-skills]]. Ingested as one body (four reference docs, one a duplicate). Raw: `raw/Clippings/`.

## What this is

Four reference pages defining the open Agent Skills format that recurs throughout this corpus as "skills" (the SKILL.md folders practitioners use to codify recurring GTM jobs):

- **Agent Skills Overview** -- what a skill is: a folder with a `SKILL.md` (metadata + instructions), optionally bundling `scripts/`, `references/`, and `assets/`.
- **Specification** -- the format: required `name` (max 64 chars, lowercase/hyphen) and `description` (max 1024 chars), optional `license`, `compatibility`, `metadata`, `allowed-tools`. Progressive disclosure: the agent loads only name + description at startup, then reads the full SKILL.md when a task matches.
- **Best practices for skill creators** -- write from real expertise, not LLM-generated generics. Extract the reusable pattern from a hands-on task: the steps that worked, the corrections you made, the input/output formats, the project-specific context the agent did not already know.
- **Optimizing skill descriptions** -- the description carries the entire triggering burden. Under-specified and it never fires; over-broad and it fires when it should not. Skills are consulted for tasks beyond what the agent handles alone (unfamiliar API, domain workflow, uncommon format), so write the description around when the skill is useful.

## Why it matters here

This is the substrate under a large share of the vault. "Skills as runbooks" is how practitioners operationalise GTM craft in [[tool-claude-code]]: [[expert-rafid-imran]] codifies each web job as a skill ([[play-code-first-marketing-site]]); [[expert-andy-toizer]]'s CRM-to-ad-strategy is a skill ([[play-crm-to-ad-strategy]]); [[expert-jared-waxman]] documents how skills silently shadow across scopes ([[concept-skill-namespacing]]). The "start from real expertise" and "carry the trigger in the description" principles are the format-level expression of [[concept-foundations-before-automation]] and [[framework-processes-first]] (document the real process before you automate it).

## Key takeaways

- A skill is a folder with a SKILL.md; everything else (scripts, references, assets) is optional.
- Progressive disclosure: name + description loaded always, body loaded on match. The description is the trigger.
- Ground skills in real, hands-on expertise; capture corrections and conventions, not generic advice.
- Best practices doc was clipped twice (identical); ingested once.

## Attribution

agentskills.io reference documentation (Anthropic Agent Skills ecosystem). No individual author. See [[tool-agent-skills]].
