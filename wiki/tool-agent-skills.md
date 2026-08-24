---
title: "Tool: Agent Skills (SKILL.md format)"
type: tool
tags: [tool, reference, ai-gtm, agentic, automation, tool-integration]
last-updated: 2026-06-13
last-updated-time: 10:30
---

# Tool: Agent Skills (SKILL.md format)

> The open format for packaging expertise an agent can load on demand. In this corpus, "skills" are how GTM engineers turn a recurring motion into a reusable, version-controlled runbook the agent runs the same way every time.

## What it is

A skill is a folder containing a `SKILL.md` file: YAML frontmatter (`name`, `description`, optionally `license`, `compatibility`, `metadata`, `allowed-tools`) plus Markdown instructions. It can bundle `scripts/`, `references/`, and `assets/`. Agents use **progressive disclosure**: at startup they load only each skill's name and description, then read the full body into context when a task matches. The `description` therefore carries the entire triggering burden. See [[source-agent-skills-docs]] for the spec and authoring guidance.

This is the format-level sibling of [[tool-mcp]]: MCP gives an agent new hands (callable tools and data); a skill gives it a documented procedure for using them.

## Position in the corpus

- **Skills as runbooks.** The dominant pattern. [[expert-rafid-imran]] codifies each recurring web job (add a case study, run the SEO/AEO preflight) as a skill so one person ships pages in hours. See [[play-code-first-marketing-site]].
- **Skills as the unit of a GTM motion.** [[expert-andy-toizer]]'s CRM-to-ad-strategy audit is a skill that reads the CRM and builds segmented paid audiences. See [[play-crm-to-ad-strategy]].
- **The namespacing trap.** Skills auto-discover across personal, project, and plugin scopes and can silently shadow one another. [[expert-jared-waxman]] commits and prefixes to defend. See [[concept-skill-namespacing]].
- **Write from real expertise.** The best-practices guidance (extract the pattern from a hands-on task; capture the corrections and conventions) is the authoring expression of [[framework-processes-first]] and [[concept-foundations-before-automation]]: document the real process before you automate it.
- **Runs inside the hub.** Skills live in [[tool-claude-code]] (and Claude Projects / Cowork), the agentic surface most of this corpus works from.

## Related

[[tool-claude-code]] | [[tool-mcp]] | [[source-agent-skills-docs]] | [[concept-skill-namespacing]] | [[play-code-first-marketing-site]] | [[play-crm-to-ad-strategy]] | [[framework-processes-first]] | [[concept-foundations-before-automation]] | [[concept-borrow-from-engineering]]
