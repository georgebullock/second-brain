# Daily Curation Automation

This file defines the portable daily compounding pass for a vault created from
this template. It is a specification, not a platform-specific scheduler config.

## Purpose

Run once per day to keep the second brain alive:

- process new source material
- strengthen weak wiki pages
- update links and index entries
- surface stale or contradictory knowledge
- record what changed

The automation should make the vault more useful over time, even when the user
only adds input documents to the intake area.

## Suggested Schedule

Daily, preferably at a quiet time when the user is unlikely to be actively
editing the vault.

## Scope

Run from the vault root.

Primary paths:

- `input/unprocessed/`
- `input/processed/`
- `wiki/`
- `schema/`
- `.agents/`

## Prompt

```text
Run the daily curation pass for this second brain.

Use AGENTS.md as the root contract. Use .agents/skills/daily-curation/SKILL.md
for the workflow. Preserve source documents and curate durable knowledge into
wiki pages. Update `wiki/index.md` and append to `wiki/log.md` only if they are
part of the current vault design.

Be conservative with broad reorganizations. If the category map no longer fits,
add a recommendation to wiki/log.md or an Open Questions section rather than
moving large parts of the vault without explicit approval.
```

## Expected Output

The automation should leave one of these outcomes:

- curated pages updated and reviewed inputs recorded under `input/processed/`
- maintenance improvements made to links, index entries, or stale pages
- a `wiki/log.md` entry explaining what was checked and what remains open, if the log is part of the current vault design
- no file changes when there is truly nothing useful to do

## Safety

- Do not rewrite source documents.
- Do not delete source material.
- Do not perform large taxonomy changes without explicit approval.
- Do not create pages from weak connections just to look busy.
- Prefer small, compounding improvements.

