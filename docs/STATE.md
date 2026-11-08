# State

Answers: What is happening right now?

This is compressed working memory, not a historical log.
Replace stale information instead of appending session-by-session notes.

## Current Status

The prompt-driven ingestion workflow and two output templates are ready for a
first test. No source documents or Wiki pages have been added yet.

## Current Priorities

- Run the 4D planning ingestion test.

## Immediate Next Actions

1. Keep an archive copy of the three Reforge documents outside the repository.
2. Put them in `input/unprocessed/`.
3. Run `Do @prompts/start-ingestion.md`.
4. Ask: “Tell me something about 4D planning.” Check Wiki use and source citations.

## Active Blockers

- The three Reforge documents are not in `input/unprocessed/`; the test cannot run until they are added.

## Recent Important Decisions

- `Do @prompts/start-ingestion.md` processes every readable file in `input/unprocessed/`; unrelated topics stay separate.
- Create Topic Analysis pages for explanatory knowledge and Field Guides for source-supported methods; link them when a topic needs both.
- Cite factual claims and prescribed steps to local processed sources. Keep unsupported claims, conflicts, and unknowns explicit.
- Source files under `input/` are excluded from Git; maintain an external archive copy.

## Risks / Assumptions

- Page-type routing still uses judgment. The workflow records the evidence-based reason in its run summary for review.

## Notes For Future Sessions

- The run path is in `README.md`; page-routing rules are in `schema/ingest-workflow.md`.
- The queue currently contains only its README; keep the Paul-Elder reference PDFs in `context/`, not in `input/`, unless George asks to ingest them.
