---
title: "Tool: litprompt"
type: tool
tags: [tool, reference, ai-gtm, automation, tool-integration]
last-updated: 2026-06-13
last-updated-time: 12:15
---

# Tool: litprompt

> A markdown preprocessor for LLM prompts, by Tom Ashworth. Treats prompts as source code: strip author-only comments and resolve imports so prompt fragments can be shared across files without copy-paste drift, while staying plain markdown.

## What it is

When system prompts, skills, and agent instructions are committed to git and deployed like software, two problems appear: HTML comments meant for the author leak into the model's view, and shared fragments (tone, tool descriptions, safety rules) get copy-pasted and drift. A template engine would solve it but breaks markdown (no GitHub rendering, hostile to non-engineers). litprompt stays inside markdown and does two things:

- **Annotated comments.** `<!-- @ ... -->` are stripped at build time (author notes, TODOs, rationale); regular HTML comments pass through.
- **Imports.** `@[label](./path.md)` is replaced with that file's contents; transitive imports resolve, frontmatter of imported files is stripped, circular imports are caught.

## Why it matters in GTM

It is the build-tooling expression of "prompts and skills are code" ([[concept-borrow-from-engineering]], [[concept-skill-namespacing]], [[tool-agent-skills]]): a way to keep shared GTM prompt fragments DRY (the same call-not-copy logic as [[concept-gtm-functions]]) and to version and comment prompts cleanly inside the repo-based workflows the corpus runs on ([[framework-strategy-as-repo]], [[concept-llm-wiki-pattern]]).

## Related

[[tool-agent-skills]] | [[concept-borrow-from-engineering]] | [[concept-skill-namespacing]] | [[concept-gtm-functions]] | [[source-tom-ashworth-personal-os]] | [[concept-llm-wiki-pattern]]
