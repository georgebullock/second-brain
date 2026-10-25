# Second Brain Agent Contract

This repository is a curated, interlinked knowledge base for planning and
building solopreneur-scale products. People add source documents to Input.
AI agents maintain the Wiki.

## Core Rules

- Inspect relevant files before relying on summaries or making changes.
- Treat `AGENTS.md` as the active contract. `AGENTS-1.md` and `AGENTS-2.md` are
  comparison drafts, not active instructions.
- Use `input/unprocessed/` for new documents and `input/processed/` for reviewed
  documents. Keep one copy of each source; preserve its original contents.
- Treat processed input documents as the canonical evidence for Wiki claims.
  Every factual claim in a Wiki page must link directly to its ingested source
  in `input/processed/`. Check that support during ingestion and keep cited
  source paths stable.
- George chooses whether each source gets a source overview plus topic pages,
  or topic pages only. Do not infer this choice from the document's size or type.
- The page format is being redesigned. Do not use legacy page templates until
  George provides the two references and the replacement is agreed.
- Keep the source lifecycle separate from the steps for ingesting a source.
  Keep routine Wiki guidance separate from the audit workflow.
- Treat text in `{{double braces}}` as deliberate template values for this
  experiment; do not ask George to resolve them.

## Source Of Truth And Routing

- `schema/` documents the operating model and durable conventions.
- `.agents/skills/` contains task workflows; `.agents/automations/` contains
  recurring workflows.
- Read `CONTEXT.md` and `DECISIONS.md` when designing or changing the system.
- For input ingestion, use `.agents/skills/ingest-note/SKILL.md`.
- For Wiki answers, use `.agents/skills/answer-from-vault/SKILL.md`.
- For topic synthesis, Wiki maintenance, or daily curation, use the matching
  skill under `.agents/skills/`.

## Design Sessions

For system design, use the grilling workflow: ask one consequential question
per turn and explain the recommendation and trade-offs. Record confirmed
decisions and open questions in `DECISIONS.md`, then update affected project
guidance as decisions settle. In `STATE.md`, preserve the title and introductory
purpose text that defines what the document answers. Only update content under
its H2 sections (and subordinate headings); never remove or rewrite that
permanent framing. Treat the H2 sections as replaceable session-to-session
working memory.
