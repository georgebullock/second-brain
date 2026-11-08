---
type: wiki_entry
entry_kind: field_guide
title: "{{Title}}"
topics: []
created_by_workflow: start-ingestion
generated:
  by: codex
  at: "{{ISO 8601 timestamp}}"
sources:
  - id: source-1
    resource: /input/processed/{{source-filename}}
    title: "{{Source title}}"
  # Add one item for every source that supports this guide.
---

# {{Title}}

Use this template when the sources provide a repeatable method, actionable
steps, decision rules, or criteria. Preserve the source's actual guidance; do
not invent or strengthen instructions. Cite each factual claim and prescribed
step to its processed source. Label source instructions, source-supported
interpretations, and cross-source synthesis distinctly. If sources disagree,
expose the disagreement and its consequences instead of forcing one procedure.

## Intended Outcome

State what the reader should be able to do after following this guide.

## When To Use

Describe the conditions where the method applies, as supported by the sources.

## Before You Start

List required information, tools, prerequisites, and constraints. If the sources
do not specify any, write “None specified.”

## Procedure

Present the method in numbered steps. Keep each step actionable and cite the
source that supports it. Mark any step synthesized across sources as synthesis.

1. {{Step and citation}}

## Decision Points And Variations

Explain choices, branches, alternatives, or disagreements that change how the
reader should proceed. Do not collapse materially different approaches.

## Rationale

Explain why the steps are recommended, using source-supported reasoning. Link
to the related Topic Analysis when one exists.

## Limitations And Failure Modes

State known limits, risks, exceptions, and conditions where the method may not
work. Do not imply certainty beyond the evidence.

## Open Questions

Record unresolved tensions, contradictions, evidence gaps, unclear points, and
questions the sources cannot answer. State what remains unknown; do not fill
gaps with guesswork. If none are material, write “None identified.”

## Sources

Use footnotes keyed to the `sources` metadata above. Cite each factual claim and
prescriptive step beside the claim.

[^source-1]: [{{Source title}}](/input/processed/{{source-filename}})

Repeat one footnote for each item in `sources`, using the same ID.

## Related Topic Analysis

Link the paired Topic Analysis when one was created. Otherwise write “None.”

- {{Topic Analysis link, or “None.”}}

## Related Topics And Connections

Record useful relationships found in the required cross-topic search. Do not
add links based only on broad topical adjacency or shared words. Explain what
connects the ideas and where the connection stops. Label cross-source
interpretations as synthesis and cite the processed sources supporting both
sides. If no useful, source-supported connection was found after the search,
write “No supported connections found.”

- [[{{Related page}}]] — {{Specific relationship and why it helps; cite the supporting source or sources.}}

## References Cited By Source

List references cited by each input source, grouped under the citing source.
Transcribe them from the source and include a page or section locator when
available. These references are leads for further reading, not evidence for
this guide unless separately processed and added under `sources`.

- {{Author-provided reference, or “No bibliography found in source.”}}
