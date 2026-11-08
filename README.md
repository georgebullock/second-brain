# Second Brain

A portable, evidence-backed knowledge base for reusable product, engineering, and solopreneur knowledge.

## First Test

Put the three Reforge course documents about 4D planning in
`input/unprocessed/`, then run `Do @prompts/start-ingestion.md`. Ask: “Tell me
something about 4D planning.” The answer must use Wiki content and cite the
processed sources.

## Run An Ingestion

1. Copy source files to `input/unprocessed/`. Keep a separate archive copy; Git ignores source files under `input/`.
2. Run `Do @prompts/start-ingestion.md`. It processes the full queue, keeping unrelated topics separate.
3. Review the run summary and generated pages. Processed source files stay local in `input/processed/` and Wiki claims link to them.
4. Ask a question from the vault using `.agents/skills/answer-from-vault/SKILL.md`.

See `AGENTS.md` for rules, `CONTEXT.md` for the pilot goal, `DECISIONS.md` for current decisions, and `schema/` for the operating model.
