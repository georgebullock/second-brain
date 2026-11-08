# Start Ingestion

Run the complete ingestion workflow for every readable source file currently
in `input/unprocessed/`.

1. Read `AGENTS.md`, `DECISIONS.md`, `schema/ingest-workflow.md`, and
   `.agents/skills/ingest-note/SKILL.md`.
2. Process every queued file. Do not ask George to restate the scope or choose a
   page format. Keep unrelated topics separate; do not skip a source because it
   is unrelated to other files in the queue.
3. Use the routing rules in `schema/ingest-workflow.md` and the matching
   template in `templates/`.
4. Preserve each source's contents and rename it using the filename convention
   in `schema/ingest-workflow.md`. Move it once to `input/processed/` with its
   final name before writing citations. Check the final citation paths after
   writing them, and report each source's original and final filename.
5. Before finalizing pages, complete the dedicated relationship-discovery pass
   in `schema/ingest-workflow.md`. Search beyond the obvious topic for
   cross-disciplinary connections, inspect candidate pages, and add only
   useful, source-supported links with an explanation. This pass is a core
   deliverable, not optional polish.
6. If a file cannot be read reliably, leave it in `input/unprocessed/` and
   report the filename and issue. Do not guess at its contents.
7. Do not modify prompts, agent instructions, schemas, or templates during an
   ingestion run.

If `input/unprocessed/` contains no source files, report that there is nothing
to process.

At the end, report each source, its topic, which page type or types were
created/updated and why, its processed status, the concepts and candidate pages
used in the relationship search, links added or why none were supported, and
any unresolved questions.
