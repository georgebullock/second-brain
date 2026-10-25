# Second Brain Context

## Purpose

Build a working v0 of a curated knowledge base for planning and building
solopreneur-scale products. The immediate goal is to try the system in practice;
it may be discarded or rebuilt if it does not work.

The Wiki must be easy for George to search and read directly, and easy for an
LLM to search and use when answering questions.

## Shared Language

- **Input**: source material brought into the system for review and possible
  curation. The current locations are `input/unprocessed/` and
  `input/processed/`.
- **Wiki**: the curated, interlinked knowledge base built from useful inputs
  and durable findings.
- **Lifecycle**: the states and locations material passes through.
- **Ingest workflow**: the actions taken to review an input and curate useful
  knowledge from it.

## Working Constraints

- Move quickly toward a usable prototype; avoid polishing speculative parts.
- Text in `{{double braces}}` is deliberate template material for this
  experiment and does not need clarification.
- The legacy page format in `schema/page-template.md` is retired. George will
  provide two replacement references before a new format is designed.
- Codex completes ingestion without a separate Wiki-page approval step. George
  reviews the resulting repository changes and can revert them and provide
  feedback.
- Review and update `README.md` after the other project files and `AGENTS.md`
  are settled.

## Current Structure

The repository currently has `input/processed/`, `input/unprocessed/`,
`schema/`, `templates/`, `wiki/`, and `.agents/`. The `wiki/` folder has no
content pages yet. Keep both processed and unprocessed locations for the v0;
how source files move or retain stable paths is open. See `DECISIONS.md`.
