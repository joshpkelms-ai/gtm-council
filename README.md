# gtm-council

An inventory of GTM thought leadership, curated by hand by me (Josh Elms), source by
source. Its two jobs: inform Claude of current best practice when it does GTM engineering
work with me, and educate the team around me on how modern revenue teams actually operate.

This is a working knowledge base, not a polished publication. I am sharing it privately as
an example of the commercial context repositories I build.

## Why it exists

Generic GTM advice from a model's training data is average and often dated. This vault is
the opposite: a small council of practitioners I picked deliberately, kept free of filler,
and structured so an agent (or a colleague) can reason over it and cite its way back to a
named source every time. The value is the curation and the structure, not the volume.

## How it is organised

- `CLAUDE.md` - the operating constitution. It tells the agent who it is, how to weigh the
  vault against outside knowledge, and the integrity rules that protect the curation
  (raw is read only, provenance is never stripped, every change is logged).
- `index.md` - the map. Every wiki page catalogued by type (expert, framework, concept,
  play, tool, source, synthesis) with a one line summary. Read first.
- `wiki/` - my synthesis. 150+ pages of derived work: what each practitioner argues, the
  named frameworks and plays, and source pages that distil each original down to its
  argument with full attribution (author and URL on every one).
- `raw/` - the immutable source material the wiki is built from. Treated as read only so
  the vault can always be rebuilt and every claim stays checkable against its origin.
- `log.md` - the audit trail. What was ingested, how it was categorised, and the calls
  made along the way.

## How to read it as a reviewer

Start with `CLAUDE.md` to see the operating principles, then `index.md` for the shape of
the corpus, then open a few `wiki/` pages that interest you (the `synthesis-` and
`concept-` pages show the reasoning best). `log.md` shows how the thing is maintained over
time, including a worked example of catching a fabricated transcript before it entered the
record.

## Provenance

The `wiki/` pages are my own writing: transformative, cited commentary over third party
material. The `raw/` folder holds the underlying sources for verification. Every source
page names its author and links its original. Nothing here is presented as mine that is not.
