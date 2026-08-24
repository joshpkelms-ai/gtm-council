---
title: "Concept: Skill namespacing and silent shadowing (Claude Code)"
type: concept
tags: [concept, ai-gtm, automation, tool-integration]
last-updated: 2026-06-12
last-updated-time: 22:30
---

# Concept: Skill namespacing and silent shadowing

> [[tool-claude-code]] auto-discovers skills from three scopes. Same-named skills collide silently, and personal beats project, so a teammate can run different logic with no warning. Commit and prefix to defend against it.

## The trap

A Claude Code skill is a folder with a SKILL.md inside. Claude Code auto-discovers skills from three places:
- personal `~/.claude`
- the project repo's `.claude`
- installed plugins

When two skills share a name, only one runs, and the precedence is **personal > project**. A personal skill silently shadows a team-committed one. No error, no warning. Output diverges across the team and the cause is hard to find.

## Two defences

- **Commit skills to `.claude/skills/`** so everyone gets the same version on `git pull`.
- **Prefix names** (e.g. `ges-`) so a personal skill cannot collide with a shared one.

## One more gotcha

The command you invoke is the **folder name**, not the `name:` in the frontmatter. Rename the folder to rename the command.

## Source

[[source-jared-waxman-claude-code-skill-shadowing]] by [[expert-jared-waxman]].

## Related

[[tool-claude-code]] | [[expert-jared-waxman]] | [[framework-strategy-as-repo]]
