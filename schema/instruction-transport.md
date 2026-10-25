# Instruction Transport

This vault uses a layered instruction system so agents can keep the wiki alive
without loading every detail into every session.

## Layers

```text
AGENTS.md
  -> always-loaded contract with cross-task rules and routing
.agents/skills/
  -> task-specific workflows
.agents/automations/
  -> recurring workflow definitions
schema/
  -> human-readable operating model
input/
  unprocessed/ -> new source material awaiting review
  processed/   -> reviewed canonical source material
wiki/
  -> maintained synthesis
wiki/index.md (proposed)
  -> navigation map
wiki/log.md (proposed)
  -> curation history
```

## Responsibilities

`AGENTS.md` answers: What must every agent know every session, including the rules for input sources, evidence links, and the Wiki?

`.agents/skills/` answers: What procedure should run for this kind of task?

`.agents/automations/` answers: What recurring agent work should happen without
waiting for a one-off prompt?

`schema/` answers: What is the durable, human-readable operating model?

`input/` answers: What source material exists, and which sources have been reviewed?

`wiki/` answers: What does the vault currently know?

## Compounding Flow

1. Source material enters `input/unprocessed/`.
2. An ingest skill turns durable pieces into `wiki/` pages.
3. The `AGENTS.md` evidence rules require direct links from factual Wiki claims to processed sources.
4. Good answers and maintenance discoveries are filed back into `wiki/`.
5. The daily curation automation checks for new sources, weak links, stale pages, and missed updates.
6. A navigation index and curation log may make later passes easier; whether
   v0 needs both is still open.

The system is working when every useful pass reduces future rediscovery.

