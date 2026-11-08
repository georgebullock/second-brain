# Maintain Wiki

Use this skill for a user-requested, on-demand health check and cleanup of the
Wiki. This is a separate workflow from ingestion and daily curation. Do not run
it automatically after ingestion.

## Workflow

1. Read `AGENTS.md`, `DECISIONS.md`, `schema/wiki-schema.md`,
   `schema/ingest-workflow.md`, and both templates in `templates/`. Use these
   files as the audit criteria; do not change them during a lint run.
2. Inventory every page in `wiki/` and review its content and outgoing links.
   If the Wiki is empty, report that there are no pages to audit.
3. Check source support. For each factual claim and prescribed step, inspect
   the cited file in `input/processed/` and verify that it supports the claim.
   Treat unavailable source files as unverifiable, not as proof a claim is
   false. Flag claims with missing, broken, indirect, or insufficient citations.
   Do not fill evidence gaps from general knowledge or web search.
4. Check consistency and currency. Compare related pages and their cited
   sources for contradictions, scope differences, and claims superseded by a
   newer processed source. Call something stale only when the vault contains
   evidence that it has been superseded; age alone is not enough.
5. Check graph quality. Find broken links, orphan pages, unexplained or weak
   links, and useful missing links between concepts. Search across topics and
   disciplines, including for shared mechanisms, complementary models,
   applications, tensions, and meaningful differences in scale. A relationship
   must help explain or use the connected ideas, and a cross-source synthesis
   must cite evidence for both sides. Do not reward link quantity or invent
   connections.
6. Check duplication and structure. Look for duplicate or near-duplicate
   pages, empty or source-less pages, inconsistent use of the two templates,
   and drift in any existing index or catalog. Do not create a new index or
   reorganize the Wiki as part of a lint run.
7. Make only clear, reversible repairs supported by the vault, such as fixing a
   link to a unique existing page or correcting a citation path when the source
   is unambiguous. Preserve evidence and meaning. For unsupported claims,
   contradictions, possible merges, weak relationships, or other judgment calls,
   report the evidence and recommended action instead of deleting, merging,
   or rewriting content.
8. Report the audit findings, any repairs made, and unresolved items. Group
   findings as `Confirmed issues`, `Review candidates`, and `No issue found`.
   For each issue, name the affected Wiki page, explain the evidence, and give a
   concrete next step. Distinguish verified problems from possibilities that
   need George's judgment. Do not start external research; list research
   questions separately for approval.

## Audit Standard

- A claim is supported only when the cited processed source directly backs it.
- A relationship is high-signal only when its specific value is explained and
  its evidence is cited. Shared labels or broad topical proximity do not count.
- An orphan or a missing page is a navigation candidate, not automatically a
  defect; recommend a new page only when the Wiki or processed sources show
  reusable knowledge that merits one.
- Report what could not be checked, including missing local source files or
  inaccessible content. Never describe an incomplete check as a clean bill of
  health.
- Keep this workflow scoped to `wiki/`. Do not ingest, move, rename, or edit
  files under `input/`; do not change prompts, skills, schemas, templates,
  project instructions, or repository structure.
