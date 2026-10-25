# Ingest Workflow

Use this workflow when turning source material into curated wiki pages.

1. Read the source document in `input/unprocessed/`.
2. Follow the curation mode George chose for this source: overview plus topic pages, or topic pages only. If no choice is recorded, ask; do not infer the mode.
3. Decide whether the source supports useful curated claims. The handling of sources with no curated claims remains an open question.
4. Search `wiki/` for related pages and near-duplicate titles.
5. Choose the best existing page to update, or create a new page if needed.
6. Preserve the original source contents and maintain one copy.
7. Record reviewed source material in `input/processed/` using the approved lifecycle. Create no Wiki citation until the canonical processed path is stable.
8. Link every factual claim directly to its processed source document.
9. Add wikilinks to related pages where useful.
10. Update `wiki/index.md` if a curated page was created or became important.
11. Add uncertainties under `Open Questions`.
12. Complete the ingest without a separate Wiki-page approval gate. George
    reviews the resulting repository changes and can revert them and provide
    feedback.

The exact transition from `input/unprocessed/` to `input/processed/` is still
being designed. Check `DECISIONS.md` before changing a source's location. Never
duplicate a source document or move a source after a Wiki page cites its path.

## Source-Only Inputs

Whether a reviewed source may remain in `input/processed/` without producing
Wiki pages is an open question. Preserve the source either way.

