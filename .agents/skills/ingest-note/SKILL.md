# Ingest Note

Use this skill to run the ingestion workflow. The normal user entry point is
`prompts/start-ingestion.md`.

Read and follow `schema/ingest-workflow.md` for batch scope, topic grouping,
page-type routing, relationship discovery, citations, and source handling.
Process every readable file in `input/unprocessed/` as one run. Do not ask
George to restate the workflow or select a format. If a source cannot be read
reliably, leave it unprocessed and report why.

Treat relationship discovery as a required, high-priority phase. Search across
Wiki topics and disciplines; do not stop at obvious neighbors. Add only useful,
source-supported links, explain the connection, and label cross-source
synthesis. At completion, report each input, topic, page type created or updated
and why, source processing status, concepts and candidate pages used in the
relationship search, links added or why no supported links were found, and
unresolved questions.
