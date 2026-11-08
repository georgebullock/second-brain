# Pilot Decisions

- Preserve one copy of each source. Review it in `input/unprocessed/`, then move it once to `input/processed/` before creating citations.
- Keep all source files in `input/` out of Git. Maintain a separate archive manually for now; its location and any automated backup are undecided. Tracked README files document the folders, but source files are local and will not appear in a fresh clone.
- The `Start Ingestion` prompt processes every readable file in `input/unprocessed/` as one run. Handle unrelated topics separately; do not drop a source just because it is unrelated to another source in the queue.
- Create a Topic Analysis for each topic with reusable knowledge. Create a Field Guide as well when the sources provide actionable steps, decision rules, criteria, or repeatable practices. Link paired pages. Do not invent instructions that the sources do not support.
- Cite every factual Wiki claim directly to its processed source. Label synthesis and interpretations clearly.
- Omit factual claims unsupported by the processed sources. Record important evidence gaps as open questions; ask for another source only when needed. Source-supported inferences are allowed and labeled.
- Show source agreements, disagreements, tensions, and contradictions in the relevant Paul-Elder sections. Preserve uncertainty; do not force a single conclusion when sources do not support one.
- Create or update topic pages for reusable knowledge by default. Add a source overview only when the source is long or multi-topic and the overview improves navigation.
- Answer from the Wiki and processed inputs. Do not fill evidence gaps from general model knowledge; ask before external research.
- Complete ingestion without a separate page approval step. George reviews the resulting changes.
- Use `templates/wiki-entry.md` for Topic Analysis pages and `templates/field-guide.md` for procedural guidance.
