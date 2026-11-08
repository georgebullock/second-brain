# Second Brain Context

## Goal

Test a portable, file-based knowledge base for evergreen business knowledge.

## Design References

Use the Paul and Elder guides in [`context/`](context/README.md) when refining
the Wiki entry structure and how pages present different perspectives.

## First Test

Put the three Reforge course documents about 4D planning in
`input/unprocessed/` and run `Do @prompts/start-ingestion.md`. Then ask: “Tell
me something about 4D planning.” The test passes when the answer uses Wiki
content and its factual claims are supported by those processed documents.
