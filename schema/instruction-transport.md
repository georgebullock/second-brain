# Instruction Transport

The user starts ingestion with one reusable prompt. The prompt runs the ingest
skill; the skill follows the schema and uses the page templates.

## Layers

```text
Do @prompts/start-ingestion.md
  -> scans the whole input/unprocessed/ queue
  -> runs .agents/skills/ingest-note/SKILL.md
  -> follows schema/ingest-workflow.md
  -> uses templates/wiki-entry.md and/or templates/field-guide.md
  -> cites local source files in input/processed/
  -> creates or updates topic pages in wiki/
```

## Responsibilities

`AGENTS.md` answers: What must every agent know every session, including the rules for input sources, evidence links, and the Wiki?

`prompts/` answers: What reusable action can George trigger with `@`?

`.agents/skills/` answers: What procedure should run for this kind of task?

`schema/` answers: What is the durable, human-readable operating model?

`templates/` answers: What structure must each output page follow?

`input/` holds the local source queue and reviewed evidence.

`wiki/` answers: What reusable knowledge has been curated?

## Compounding Flow

1. George copies source files into `input/unprocessed/` and keeps a separate archive copy.
2. George triggers `prompts/start-ingestion.md` once for the whole queue.
3. The workflow processes each readable source, keeps unrelated topics separate, and moves reviewed sources to `input/processed/`.
4. Wiki pages cite those local processed files; all source files are excluded from Git.
5. George reviews the resulting Wiki pages and run summary.

