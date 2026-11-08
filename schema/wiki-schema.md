# Wiki Schema

This repository turns local source files into cited, reusable Wiki knowledge.
The Wiki is organized by topic. Each page uses one of two standard formats so
readers can understand the reasoning, practical method, evidence, and
uncertainty.

The vault is intended to work well in Obsidian. Optimize for readable filenames,
wikilinks, backlinks, aliases, tags, and a useful graph.

## Layers

- `input/unprocessed/` contains newly added local source material awaiting review; source files are excluded from Git.
- `input/processed/` contains reviewed local source documents and canonical evidence; source files are excluded from Git.
- `wiki/` contains curated topic pages synthesized from processed input sources.
- `templates/` contains the Topic Analysis and Field Guide formats.
- `schema/` contains the durable operating rules and workflows.
- `prompts/` contains user-facing workflow launchers.
- `.agents/skills/` contains the procedures run by those launchers.

## Compounding Principle

The wiki should become more valuable with every useful interaction. An agent
should not only answer questions or summarize sources; when the result is durable,
it should improve the maintained artifact.

Examples of compounding work:

- an input source contributes to one or more curated pages
- a good answer becomes a new section or page
- a disagreement appears in the relevant analysis sections and in `Open Questions` when unresolved
- a repeated search reveals a topic that needs a clearer or linked page
- a loose note becomes a link to an existing person, place, project, decision, or concept
- a maintenance pass removes duplication and improves navigation

## Curated Pages And Evidence

Topic Analysis pages use the Paul-Elder Elements of Thought to explain ideas,
reasoning, and differing perspectives. Field Guides capture source-supported
methods and decision rules. Create both when a topic has useful analysis and an
actionable method; link the pages. Keep complexity, tensions, contradictions,
and unknowns visible. Do not imply certainty beyond the evidence.

Every factual claim and prescribed step must link directly to its supporting
document in `input/processed/`. A Wiki page is a synthesis, not a substitute for
the source. Compare each claim with the source during ingestion.

Use `templates/wiki-entry.md` for Topic Analysis pages and
`templates/field-guide.md` for procedural guidance. Each template has the same
source metadata and citation requirements.

## Input Sources

Input documents may be messy, emotional, generated, obsolete, or unclear.
Preserve the original contents and keep one local copy of each source in
`input/`. Maintain a separate archive manually for now. Do not rewrite sources
for style or category fit. Create or update curated pages in `wiki/` when
useful. Source files are excluded from Git, so a fresh clone will not include
the files behind Wiki citations. The tracked README files only explain the
input folders.

## Relationships And Cross-References

The Wiki is a conceptual graph, not only a collection of pages grouped by
subject. Look for supported relationships across topics and disciplines so
readers can follow ideas between fields and build a lattice of knowledge.

Useful relationships include:

- A shared mechanism or pattern appears in different fields.
- One model offers a useful analogy for another, with its limits made clear.
- One topic complements, qualifies, applies, or challenges another.
- A source or concept affects multiple topics, or a page depends on a person,
  place, project, decision, routine, or source described elsewhere.

Create a cross-reference only when it helps explain or use the connected ideas.
Shared words, broad category membership, or an obvious adjacency alone do not
justify a link. Explain the relationship in plain language. If the connection
is a cross-source synthesis rather than a link stated by an author, label it as
synthesis and cite evidence from both processed sources. State where an analogy
stops applying. Do not force a link when the sources do not support one.

Use Obsidian links so readers can move between pages and inspect backlinks:

```markdown
See also: [[Related Page]]
```

Use aliases when the displayed text should differ:

```markdown
See also: [[Related Page|display text]]
```

The paired Topic Analysis and Field Guide link to each other when both exist.
During ingestion, complete the relationship search in
`schema/ingest-workflow.md`; the paired-page link does not replace that search.
