# Daily Curation

Use this skill for the recurring maintenance pass that keeps the second brain
compounding.

## Workflow

1. Read `AGENTS.md`, `schema/wiki-schema.md`, and `schema/category-map.md`. Read `wiki/index.md` if it exists.
2. Inspect `input/unprocessed/` for new source material.
3. If new source material exists, process a manageable batch with `.agents/skills/ingest-note/`.
4. Search for wiki pages that are missing sources, missing index entries, or have unresolved `Open Questions`.
5. Check whether recent sources should update existing pages instead of creating new ones.
6. Improve cross-links when proper nouns, projects, places, concepts, or decisions recur.
7. Update `wiki/index.md` when navigation changes if the index is part of the current vault design.
8. Append meaningful work, skipped work, and recommendations to `wiki/log.md` if the log is part of the current vault design.

## Priority Order

1. Preserve source documents and keep one copy of each.
2. Curate high-signal new material.
3. Update existing pages before creating new pages.
4. Improve links and index entries.
5. Record open questions and maintenance recommendations.

## Batch Limits

Keep daily passes modest. If there are too many input documents to process safely,
process the highest-signal batch and record what remains in `wiki/log.md` if the
log is part of the current vault design.

## Log Entry Format

```markdown
## YYYY-MM-DD

- Inputs reviewed:
- Updated:
- Sources recorded as processed:
- Open questions:
- Next pass:
```

