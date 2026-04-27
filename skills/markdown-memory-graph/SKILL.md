---
name: markdown-memory-graph
description: Create, maintain, validate, and retrieve Obsidian-style Markdown memory graphs for LLM-assisted software projects and LLM-powered applications. Use when a project needs durable project memory, build-time agent context, runtime LLM memory design, hallucination reduction through provenance/status/confidence, or compact context-pack generation from linked Markdown notes.
---

# Markdown Memory Graph

Use this skill to add a portable Markdown memory layer to a project.

## Classify The Project

Choose the smallest useful mode:

- Build-time memory: AI helps develop the project, but the app does not use AI at runtime.
- Runtime memory: the app uses LLMs as part of product behavior.
- Hybrid: both are needed.

## Inspect First

Read the existing project instructions, docs, schemas, tests, scripts, and current memory conventions before adding a vault. Prefer extending existing project docs over inventing parallel conventions.

## Build-Time Vault

Create `docs/llm-memory/` with focused notes:

```text
index.md
decisions/
constraints/
gotchas/
workflows/
domain-facts/
open-questions/
```

Each note should be atomic and source-backed. Use frontmatter with:

```yaml
id: stable-note-id
type: decision | constraint | gotcha | workflow | domain-fact | open-question | runtime-memory
status: confirmed | inferred | disputed | deprecated | open-question
confidence: high | medium | low
source:
  - path/to/source.md
links:
  - [[related-note-id]]
last_verified: YYYY-MM-DD
```

## Runtime Memory

For LLM-powered apps, recommend durable app storage instead of Markdown as the runtime source of truth:

- event log for raw user/model/system events
- memory notes with scope, status, confidence, and source event IDs
- typed links between memory notes
- retrieval service that builds a compact memory pack
- prompt injection point that separates canon facts from inferred notes

## Retrieval Rules

A memory pack should:

- include directly matched notes
- expand `[[links]]` one hop
- include source and status metadata
- exclude deprecated notes by default
- surface disputed notes as warnings
- label inferred notes separately from confirmed facts

## Update Project Instructions

After adding a vault or retrieval script, update the repo's agent instructions or README with how to consult it before making changes.
