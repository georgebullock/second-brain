# Wiki Schema

This repository is a second brain maintained from input documents, exports,
conversations, and other source material. The goal is not to perfectly file
everything on the first pass. The goal is to preserve sources, then gradually
curate them into reliable, useful pages that compound over time.

The vault is intended to work well in Obsidian. Optimize for readable filenames,
wikilinks, backlinks, aliases, tags, and a useful graph.

## Layers

- `input/unprocessed/` contains newly added source material awaiting review.
- `input/processed/` contains reviewed source documents and canonical evidence.
- `wiki/` contains curated pages synthesized from processed input sources.
- `schema/` contains maintenance instructions, templates, category definitions, and workflow notes.
- `.agents/` contains agent-facing automation definitions, rules, and task workflows.

## Compounding Principle

The wiki should become more valuable with every useful interaction. An agent
should not only answer questions or summarize sources; when the result is durable,
it should improve the maintained artifact.

Examples of compounding work:

- an input source contributes to one or more curated pages
- a good answer becomes a new section or page
- a contradiction becomes an `Open Questions` item
- a repeated search becomes an index entry or hub page
- a loose note becomes a link to an existing person, place, project, decision, or concept
- a maintenance pass removes duplication and improves navigation

## Curated Pages And Evidence

Curated pages should be concise, readable, and useful for both human search and
LLM retrieval. Every factual claim must link directly to its supporting document
in `input/processed/`. A Wiki summary is not a substitute for the canonical
source. Compare each claim with its source during ingestion.

The page structure and frontmatter are being redesigned. Do not use the legacy
shape in `schema/page-template.md` until the replacement is agreed.

## Input Sources

Input documents may be messy, emotional, generated, obsolete, or unclear.
Preserve the original contents and keep one copy of each source in this project.
Do not rewrite sources for style or category fit. Create or update curated
pages in `wiki/` when useful.

## Cross-References

The wiki should become interlinked over time.

Use cross-references when:

- a source affects more than one topic
- a topic appears in several contexts
- a page summarizes or updates an older page
- a page depends on a person, place, project, decision, routine, or source described elsewhere
- an input source should inform multiple curated pages

Prefer links over duplication:

```markdown
See also: [[Related Page]]
```

Use aliases when the displayed text should differ:

```markdown
See also: [[Related Page|display text]]
```

The exact placement of related links is part of the page format being redesigned.

## Index

The current schema proposes `wiki/index.md` as a content-oriented catalog.
Whether v0 needs an index and when to update it remain open; see `DECISIONS.md`.

## Log

The current schema proposes `wiki/log.md` for curation history. Whether v0
needs a log remains open; see `DECISIONS.md`.
