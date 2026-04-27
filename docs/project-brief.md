# Project Brief

## Concept

Use Obsidian-style Markdown graphs as a portable memory layer for LLMs.

The memory layer stores small, addressable notes with explicit provenance, confidence, status, and links. Retrieval tooling compiles the relevant notes into a compact context pack for an LLM instead of dumping long documents or chat history into context.

## Primary Use Cases

### Build-Time Memory

For projects where AI is used to build the software, but not in the application runtime.

Examples:

- architecture decisions
- migration policies
- coding conventions
- test workflows
- deployment constraints
- user/project preferences
- known gotchas
- open questions

### Runtime Memory

For applications where an LLM is part of the product experience.

Examples:

- durable event logs
- user preferences
- world facts
- character state
- unresolved story threads
- source-grounded memory notes
- retrieved context injection

## Hallucination Controls

The system must distinguish:

- `confirmed`: supported by explicit source or durable app state
- `inferred`: plausible but not guaranteed
- `disputed`: conflicting or questioned
- `deprecated`: known stale or superseded
- `open-question`: not yet known

LLMs should treat confirmed notes as canon, inferred notes as soft context, disputed notes as warnings, and deprecated notes as non-authoritative.

## Core Pipeline

```text
source material -> atomic notes -> typed links -> retrieval pack -> grounded LLM context
```

## Generic Vault Structure

```text
docs/llm-memory/
  index.md
  decisions/
  constraints/
  gotchas/
  workflows/
  domain-facts/
  runtime-memory/
  open-questions/
```

## Retrieval Pack Requirements

A context pack should include:

- matching notes
- one-hop linked notes
- source/provenance lines
- status and confidence
- warnings for disputed notes
- exclusion of deprecated notes unless explicitly requested
