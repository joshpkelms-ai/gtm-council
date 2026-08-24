---
title: "Source: Jared Waxman -- A Claude Code skill is just a folder, and it can silently shadow"
type: source
tags: [source, ai-gtm, automation, tool-integration]
source-title: "A Claude Code skill is just a folder with a SKILL.md inside"
source-url: https://www.linkedin.com/posts/jwaxman_a-claude-code-skill-is-just-a-folder-with-activity-7466204044735246336-vHmL
source-author: Jared Waxman
source-published: unknown
raw-path: raw/Jared Waxman/2.md
last-updated: 2026-06-12
last-updated-time: 22:30
---

# Source: Jared Waxman -- A Claude Code skill is just a folder, and it can silently shadow

> LinkedIn post by [[expert-jared-waxman]]. Raw: `raw/Jared Waxman/2.md`.

## Summary

A [[tool-claude-code]] skill is a folder with a SKILL.md inside. The trap: Claude Code auto-discovers skills from three places -- personal `~/.claude`, the project repo's `.claude`, and installed plugins. When two skills share a name, only one runs, and personal beats project. So a personal skill silently shadows a team-committed one with no warning -- you run different logic from your teammates and only find out when output diverges.

Two cheap defences:

- Commit skills to `.claude/skills/` so the whole team gets the same version on `git pull`.
- Prefix names (his cohort uses `ges-`) so a personal skill cannot collide with a shared one.

One more gotcha: the command you invoke is the folder name, not the `name:` in frontmatter. Rename the folder to rename the command.

## Key takeaways

- See [[concept-skill-namespacing]]: scope precedence (personal > project > plugin) causes silent shadowing.
- Commit and prefix to keep a team running identical logic.
- Folder name is the command, not the frontmatter name.

## Attribution

[[expert-jared-waxman]], Founder of GTM Engineer School. Cheatsheet made for Cohort 4 students. Original LinkedIn post.
