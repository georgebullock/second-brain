# Second Brain Agent Contract

## Purpose

This repository is a curated, interlinked knowledge base for planning and building solopreneur-scale products. People add source documents to Input. AI agents read those sources and maintain the Wiki.

## Mission And Working Area

- Keep `ai/` as the primary workspace for drafts, analyses, alternatives, replacement proposals, and temporary working materials.
- Create or update durable, source-backed knowledge in `wiki/` as part of the repository's core job.
- Keep source documents in `input/`; preserve their original contents and maintain one local copy of each. Do not use `ai/` to duplicate source documents.
- Read project files as needed, including protected files. Reading a file does not authorize changing it.

## Change Boundaries

### Routine Work That Is Authorized

- Read files anywhere in the repository.
- Create or update Topic Analysis and Field Guide pages in `wiki/` when a user-triggered workflow or direct request calls for that knowledge work. Search for a suitable page before creating a new one.
- Keep existing Wiki content when it is still useful and supported by sources. Make focused updates; avoid replacing whole pages unless George asks.
- During a run started with `prompts/start-ingestion.md`, process readable files from `input/unprocessed/` according to `schema/ingest-workflow.md`. Move a reviewed source once to `input/processed/` before citing it; preserve its contents and keep cited paths stable.
- Update `docs/STATE.md` only when George invokes `prompts/handoff-session.md`. Preserve its title and introductory purpose text; update only content under its existing H2 sections.
- Put other drafts, working materials, and proposals in `ai/`.

### Protected Project Files

Treat all project files as read-only except for the routine work listed above. In particular, do not edit or replace:

- `AGENTS.md`, `CONTEXT.md`, `DECISIONS.md`, or project `README.md` files.
- Anything under `context/`, `prompts/`, `.agents/`, `schema/`, or `templates/`.
- Any file under `docs/` other than the narrow `docs/STATE.md` handoff exception above.
- Source documents, project configuration, scripts, or repository structure.

Changes to project instructions, workflows, prompts, schemas, templates, configuration, features, or repository structure require George's explicit approval. A broad task request is not approval to change a protected path. Explicit approval names the restricted action or path. Until approval is given, prepare any suggested replacement or patch in `ai/` and wait for George to promote it.

Keep existing names, document roles, workflows, and canonical locations. Do not add a top-level folder or a new document system without explicit approval. Follow direct user instructions when they explicitly authorize a restricted action or path. When context is incomplete, state assumptions instead of inventing project requirements.

## Source And Evidence Rules

- Treat processed input documents as the canonical evidence for Wiki claims. Link every factual claim and prescribed step directly to its supporting source in `input/processed/`; verify support while writing and keep cited paths stable.
- Do not rewrite source documents. Keep one copy of each and preserve the original contents.
- When answering from the vault, use the Wiki and processed sources. Do not fill evidence gaps with general model knowledge. If neither supports an answer, say that no ingested sources cover it and that you cannot answer from the vault. Offer external research or a research sub-agent only as an option, and wait for George's approval before starting.
- Curate reusable knowledge into topic pages by default. Add a source overview only when the source is long or multi-topic and an overview improves navigation for George or an LLM.
- Follow `schema/ingest-workflow.md` to choose the Topic Analysis and/or Field Guide template. Keep source lifecycle guidance separate from ingestion steps, and routine Wiki guidance separate from audit workflow.
- Treat text in `{{double braces}}` as deliberate template values; do not ask George to resolve them.
- If the project has writing or style guidance for the requested artifact, read and follow it before drafting. A direct user instruction takes precedence over that guidance.

## Sources Of Truth And Routing

- `schema/` describes the operating model and durable conventions; `prompts/` contains user-triggered workflow launchers; `.agents/skills/` contains task procedures.
- Read `CONTEXT.md` and `DECISIONS.md` when preparing a system-change proposal. Do not edit them without explicit approval.
- For input ingestion, follow `prompts/start-ingestion.md`, which routes to `.agents/skills/ingest-note/SKILL.md`.
- For Wiki answers, use `.agents/skills/answer-from-vault/SKILL.md`.
- For topic synthesis, Wiki maintenance, or daily curation, use the matching skill under `.agents/skills/`.

## System-Change Proposals

When George asks to discuss or design a system change, use the grilling workflow: ask one consequential question per turn and explain the recommendation and trade-offs. Record confirmed decisions and open questions as a proposed update in `ai/`. Prepare proposed edits to affected project guidance in `ai/` as well. Do not change `DECISIONS.md` or other protected project files until George explicitly approves the named changes.

## Git And Review Conventions

- Use Conventional Commits for AI-authored commit messages and pull request titles.
- Suffix every AI-authored commit message with ` [AI]` (for example, `docs: propose agent contract [AI]`).
- Prefix an AI-authored pull request title with `[AI]`.
- When the project uses review-style feedback, use Conventional Comments where applicable.

## Workflow-Scoped Document Updates

This is a narrow exception to the protected-file rule above. When George triggers an established workflow, update the minimum relevant workflow documents needed to complete that workflow. This may include prompts, skills, schemas, templates, and other task-specific operating documents. Make only the changes required to carry out the requested workflow; this does not authorize unrelated cleanup, new features, or broader changes to how the system works.

Examples of workflow documents covered by this exception are `prompts/start-ingestion.md`, `prompts/start-session.md`, `prompts/handoff-session.md`, files under `.agents/skills/`, `schema/ingest-workflow.md`, `schema/wiki-schema.md`, and files under `templates/`. These are not routine update targets; change them only when needed to complete the triggered workflow. Other task-specific workflow documents follow the same rule.

This exception does not apply to `AGENTS.md`, `README.md`, `CONTEXT.md`, or `DECISIONS.md`. `docs/STATE.md` remains editable only when George invokes `prompts/handoff-session.md`, and only under its existing H2 sections. Files under `context/` remain read-only. Keep `ai/` ignored by default to keep work in progress out of Git; track individual files from `ai/` only when needed for review or as an approved deliverable. If it is unclear whether a change is necessary to complete the triggered workflow, prepare a proposal in `ai/` and ask George before editing the file.
