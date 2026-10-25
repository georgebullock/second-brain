# Ingest Note

Use this skill when processing new input documents, transcripts,
clips, exports, or conversation summaries.

## Workflow

1. Inspect `input/unprocessed/`.
2. Read the relevant source material.
3. Follow the curation mode George chose for this source: create a source overview plus topic pages, or topic pages only. If no choice is recorded, ask; do not infer the mode.
4. Search `wiki/` for related pages, duplicate titles, people, places, projects, and recurring topics.
5. Create a new curated page only if no suitable page exists.
6. Prefer updating an existing page over creating a near-duplicate.
7. Ensure the reviewed source is recorded in `input/processed/` using the approved lifecycle. Check `DECISIONS.md` for current lifecycle rules. Never make a duplicate source copy.
8. Link every factual claim directly to the processed source document. Verify each claim against that document during ingestion.
9. Add wikilinks to related pages where useful.
10. Update `wiki/index.md` if a curated page was created, renamed, merged, or became important.
11. Complete the ingest without pausing for separate Wiki-page approval. George reviews the resulting repository changes and can revert them and provide feedback.

## Output

Summarize:

- Which input files were processed.
- Which wiki pages were created or updated.
- Which sources were recorded as processed.
- Any open questions or uncertain categorization.

