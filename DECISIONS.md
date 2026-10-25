# Decisions

Confirmed choices are listed first. **Open Questions** are unresolved and must
not be treated as settled. Current status and next steps live in `STATE.md`.
Promote durable architectural choices to ADRs when the design is stable.

## Confirmed Decisions

| Decision | Rationale |
| --- | --- |
| Use **Input** and **Wiki** as the concepts for source material and curated knowledge. | These names match how George thinks about the two layers. |
| Keep `input/unprocessed/` and `input/processed/` for the prototype. | A visible intake queue and reviewed-source area are useful; their exact file lifecycle is still open. |
| Give core actions quick, reusable launchers. | They reduce repeated voice and typing. `@` file selection and `$` skill invocation both work; the exact invocation method is not a project decision. |
| A person chooses each source's curation mode: source overview plus topic pages, or topic pages only. | The LLM must not infer this from source size or type. |
| Every factual claim in generated documents should link directly to its ingested source in `input/processed/`; this is non-negotiable for Wiki pages. | George must be able to inspect the canonical source and verify each claim. A Wiki summary is not a citation substitute. |
| Build claim-to-source checking into ingestion. | The workflow must compare claims with the ingested source and attach its reference while creating or updating Wiki content. |
| Keep each input source as one file in the project. | Duplicate copies are out of scope. |
| Keep cited source paths stable. | Broken evidence links are unacceptable. |
| Keep the source lifecycle separate from the ingest procedure. | Locations and review states differ from the steps that process a source. |
| Ingest review timing (Q3): Codex completes ingestion without a separate Wiki-page approval gate; George reviews the resulting repository changes and can revert them and provide feedback. | A pre-write approval step interrupts ingestion, while a separate post-write approval loop adds work when George can inspect and revert the changes directly. |
| Keep everyday wiki/page guidance separate from the wiki audit checklist. | Creating and maintaining pages is routine work; linting is a specific review task. |
| Replace the current page entry format using two references George will provide. | The format in the draft is obsolete and should not shape v0. |
| Review the README after the other project files and `AGENTS.md` are finalized. | The README describes a system that is still being reconciled. |

## Open Questions

1. **Input lifecycle and source paths:** How should the system track intake, review, and processed status while keeping one source file and preventing citations from breaking? Decide whether sources move, stay at stable paths with status tracked separately, or use another mechanism. The physical layout and lifecycle are parked until this is resolved.
2. **Per-source curation mode:** How does George mark a source for an overview plus topic pages or for topic pages only? The choice must be explicit before ingest. Its mechanism depends on the Input lifecycle decision.
4. **Citation format:** What exact page structure and citation syntax will make every factual claim link directly to its ingested source? The current entry format is obsolete; wait for the two references before designing it.
5. **Unsupported claims:** If a useful factual claim has no support in an ingested source, should ingestion omit it, record it as an open question, or ask George to add a source?
6. **Citation checker:** Should a deterministic script check citation syntax and target paths, and when should it run? Human review must still check whether each source actually supports its claim.
7. **Wiki organization and navigation:** What categories, page types, index, and log best support both George's keyword search and LLM retrieval? The current category map is generic, and `wiki/` has no content pages yet.
8. **Agent instruction routing:** What belongs in always-loaded `AGENTS.md` versus `schema/`, skills, or automations? Decide what to do with the current `Rules` section and which workflows need routing pointers.
9. **Core action launchers:** Which actions need reusable launcher files, and where should those files live? The need for quick launchers is settled; the exact set and structure are not.

