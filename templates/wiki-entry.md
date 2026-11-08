---
type: wiki_entry
entry_kind: topic_analysis # use source_overview only when it improves navigation
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
  # Add one item for every source that supports this page.
---

# {{Title}}

Use this template to teach the reader a topic by analyzing its reasoning with
the eight Elements of Thought below. With multiple sources, attribute each
source's reasoning in the relevant sections and identify agreements, conflicts,
and differences. Represent each perspective fairly. Do not flatten, dumb down,
or reduce complex reasoning to false agreement, false certainty, or a single
simple conclusion. Expose tensions, contradictions, evidence gaps, and unknowns;
do not force a resolution the sources do not support. Label interpretations and
cross-source conclusions as synthesis, distinguish them from what each source
states, and do not imply greater certainty than the evidence supports. Cite
factual claims to their processed sources.

## 1. Purpose

State as accurately as possible what the author was trying to accomplish.

## 2. Question At Issue

Identify the key question the author was addressing.

## 3. Information

Identify the most important information the author used or presupposed to
support the main argument: facts, experiences, and data.

## 4. Inferences

Identify the most important conclusions the author presents. Keep any
additional conclusions drawn across sources clearly labeled as synthesis.

## 5. Concepts

Identify the key ideas needed to understand the author's reasoning. Explain
what the author means by them.

## 6. Assumptions

Identify what the author takes for granted that could be questioned. Surface
implicit assumptions when the source's reasoning supports that interpretation.

## 7. Implications

### 7a. If We Take This Line Of Reasoning Seriously

What consequences are likely to follow? Include implications the author states
and implications that follow from the author's position.

### 7b. If We Fail To Take This Line Of Reasoning Seriously

What consequences are likely to follow if people ignore the author's reasoning?

## 8. Point Of View

Identify what the author is looking at and how the author is seeing it.

## Open Questions

Record unresolved tensions, contradictions, disagreements, evidence gaps,
unclear points, and questions the sources cannot answer. State what remains
unknown; do not fill gaps with guesswork. Ask for another source only when
needed. If there are no material open questions, write “None identified.”

## Sources

Use one footnote per source, keyed to the `sources` metadata above. Add a
citation beside each factual claim so the reader can check it against the
processed source.

[^source-1]: [{{Source title}}](/input/processed/{{source-filename}})

Repeat one footnote for each item in `sources`, using the same ID.

## References Cited By Source

List references cited by each input source, grouped under the citing source.
Transcribe them from the source and include a page or section locator when
available. These references are leads for further reading, not evidence for
this Wiki entry unless separately processed and added under `sources`.

- {{Author-provided reference, or “No bibliography found in source.”}}

## Related Field Guide

Link the paired field guide when one was created. Otherwise write “None.”

- {{Field guide link, or “None.”}}

## Related Topics And Connections

Record useful relationships found in the required cross-topic search. Do not
add links based only on broad topical adjacency or shared words. Explain what
connects the ideas and where the connection stops. Label cross-source
interpretations as synthesis and cite the processed sources supporting both
sides. If no useful, source-supported connection was found after the search,
write “No supported connections found.”

- [[{{Related page}}]] — {{Specific relationship and why it helps; cite the supporting source or sources.}}
