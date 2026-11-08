# Ingest Workflow

`prompts/start-ingestion.md` starts this workflow for every readable source
file in `input/unprocessed/`. Do not ask George to repeat the scope or select
page types during a normal run.

## Scope And Grouping

- Process every supported file in the queue. If one file cannot be read
  reliably, leave it unprocessed and report why.
- Review sources independently, then group reusable claims by topic. Combine
  sources only when they address the same topic; keep unrelated topics
  separate.
- Search `wiki/` before creating pages. Update a suitable page rather than
  making a duplicate.
- If a source has no reusable knowledge, move it to `input/processed/` without
  creating a Wiki page.

## Source Filename Convention

Give every successfully processed source a clear, subject-first filename:

`<Broad Topic> - <Specific Topic or Method> - <Descriptive Title>.<original extension>`

- Use the broad topic first, followed by the specific topic, method, or subtopic, then what the document covers. For example: `Product Roadmaps - 4D Roadmaps - The 4 Lenses.pdf`.
- Use one primary broad topic for the filename. Represent cross-cutting topics with Wiki links or metadata rather than duplicate source files.
- Omit a hierarchy level when it adds no meaning; do not invent a topic or method just to fill a segment.
- Keep a useful title from the source. If it has no clear title, derive a short, accurate title from its contents.
- Remove capture numbers, download-tool labels, URLs, and other filename clutter. Do not add dates routinely; retain a date or version only when it is meaningful to the source's identity or interpretation.
- Preserve the original extension and file contents. If the resulting name collides with another file, add the shortest useful distinguishing detail to the title.

## Page-Type Routing

- Create or update a **Topic Analysis** for each topic with reusable
  explanatory knowledge. Use `templates/wiki-entry.md` and the eight Elements
  of Thought.
- Also create or update a **Field Guide** when the sources provide actionable
  steps, decision rules, criteria, or repeatable practices. Use
  `templates/field-guide.md`.
- Create both when a topic has substantial explanatory knowledge and an
  actionable method. Link the pair. Do not make a Field Guide from vague advice
  or add a Topic Analysis that contains no useful reasoning.
- Include a short routing reason in the run summary, based on observable
  features of the sources (for example: named concepts and arguments; numbered
  steps, decision criteria, or repeatable practices).
- Add a source overview only when a long or multi-topic source needs one for
  navigation. Use the Topic Analysis structure and identify it as a source
  overview in frontmatter.

## Relationship Discovery

This is a required phase of every ingestion and has equal priority with accurate,
auditable source synthesis. Give it a dedicated pass before completing the run;
do not treat links as optional polish after writing the pages.

1. Identify the source's important concepts, models, mechanisms, causal
   patterns, constraints, and decision rules—not only its subject labels.
2. Search existing Wiki pages using both the source's terms and the underlying
   ideas. Search across broad topics and disciplines. Do not stop at the first
   obvious same-topic match; inspect plausible connections further afield.
3. Test whether each candidate page has a useful relationship to the source or
   new page: for example, a shared mechanism, a useful analogy with stated
   limits, a complementary perspective, a different scale, a dependency, or a
   tension or contradiction. Broad topical adjacency or shared words alone are
   not enough.
4. Add a Wiki link when the relationship helps the reader understand either
   topic or transfer an idea between them. Explain the specific connection and
   its limits, and cite the processed sources supporting both sides. Label a
   connection developed by comparing sources as `Synthesis`; do not present it
   as something either author stated.
5. Use the new page's Related Topics And Connections section for each useful
   link. Obsidian backlinks provide reverse navigation; add a reciprocal entry
   to an existing page only when it improves that page's navigation.
6. Do not invent a connection to fill the section. If the search finds no
   useful, source-supported connection, say so in the section and run summary.

Spend time on this pass. Search for conceptual structure across the Wiki, not
only direct neighbors. The goal is a useful lattice of supported connections,
not the largest number of links.

## Source And Evidence Rules

1. Preserve the original contents and one local copy of each source.
2. After reviewing a source, assign its final filename using the convention
   above, then rename and move it in one operation from `input/unprocessed/` to
   `input/processed/`. Do this before creating citations. Never rename or move
   the source after a Wiki page cites its path.
3. Verify every factual claim and prescribed step against the processed source.
   Cite the supporting source beside the claim. Label source-supported
   interpretation and cross-source synthesis.
4. Omit unsupported factual claims. Preserve disagreements, contradictions,
   tensions, evidence gaps, and unknowns in the relevant page sections and
   `Open Questions`; do not force a resolution or imply certainty the evidence
   does not support.
5. Do not treat references listed by a source as evidence unless those works
   are separately processed and cited.

All source files under `input/` are excluded from Git. Keep a separate archive
copy manually. Wiki links resolve to the local source files; a fresh Git clone
will not contain those files.

## Run Summary

Report each input file's original and final filename, topic, page type created
or updated, the evidence-based reason for that page type, whether the source
moved to `input/processed/`, the main concepts or mechanisms used in the
relationship search, candidate pages reviewed across topics, useful links added
(or why none were supported), and any unresolved questions or files left
unprocessed.
