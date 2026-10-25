# State

Answers: What is happening right now?

This is compressed working memory, not a historical log.
Replace stale information instead of appending session-by-session notes.

## Current Status

The v0 design is being reconciled before the prototype is used. `AGENTS.md` now
contains the settled core rules. The Wiki has no content pages; `wiki/index.md`
and `wiki/log.md` are not present.

## Current Priorities

- Resolve the high-impact ingest and source-traceability choices in
  `DECISIONS.md`.
- After the lifecycle decision, align the documented folder structure and
  ingest workflow.
- Design the new Wiki page format after George provides the two references.
- Finish project guidance before reviewing `README.md`; README review is last.

## Immediate Next Actions

Ask whether ingest should pause for George's approval before writing Wiki pages,
or create source-checked pages and present them for review afterward (Open
Question 3 in `DECISIONS.md`).

## Active Blockers

- Page-format redesign is waiting on two references from George.
- Source lifecycle, citation syntax, and ingest review timing remain unresolved;
  do not finalize the ingest workflow around assumptions about them.

## Recent Important Decisions

- Use `input/` and `wiki/`; keep `input/unprocessed/` and `input/processed/` for
  the prototype.
- Keep one copy of each source and keep cited paths stable. The exact lifecycle
  and path strategy remain open.
- George chooses each source's curation mode: overview plus topic pages, or
  topic pages only.
- Every factual Wiki claim must link to an ingested source in
  `input/processed/`; check support during ingest. Links enable human review;
  automated checks cannot prove semantic support.
- Keep lifecycle rules separate from ingest steps, and routine Wiki guidance
  separate from audit guidance.

## Risks / Assumptions

- Broken or unstable source links would defeat the required fact-checking path.
- A script may check citation presence and path resolution, but a human still
  needs to confirm that a source supports its claim.

## Notes For Future Sessions

- `AGENTS-1.md` and `AGENTS-2.md` are comparison drafts, not active guidance.
- The routed `.agents/skills/` workflows and daily-curation automation exist.
- Research on source summaries is in
  `ai/research/source-summaries-and-topic-pages.md`.
- Promote durable architectural choices to ADRs when the design is stable.
- Replace stale status, priorities, next steps, and blockers here. Keep durable
  choices and unresolved design questions in `DECISIONS.md`.
