# LLMProjectMemory

Portable Markdown memory graphs for LLM-assisted projects and LLM-powered applications.

This repository captures a reusable pattern inspired by Obsidian-style linked Markdown notes:
small, provenance-backed knowledge units connected by typed links and compiled into compact context packs for LLMs.

Target GitHub repository: `ochssoft/LLMProjectMemory`.

## Goals

- Reduce repeated project rediscovery during AI-assisted development.
- Preserve decisions, constraints, workflows, gotchas, and open questions in human-editable Markdown.
- Build compact retrieval packs for Codex, Claude Code, Cursor, Continue, local Ollama workflows, or custom LLM apps.
- Support runtime memory designs for applications where LLM continuity matters.
- Reduce hallucination risk by distinguishing confirmed, inferred, disputed, deprecated, and open-question notes.

## Initial Shape

- `docs/project-brief.md` explains the core concept and project scope.
- `docs/example-project-prompts.md` preserves the first concrete rollout prompts for existing projects.
- `skills/markdown-memory-graph/` is the planned reusable Codex skill.

## Memory Model

A memory vault is usually placed inside a project at `docs/llm-memory/` and contains atomic Markdown notes with frontmatter:

```yaml
---
id: stable-note-id
type: decision
status: confirmed
confidence: high
source:
  - path/to/source.md
links:
  - [[related-note]]
last_verified: 2026-04-27
---
```

The key rule is that Markdown files are not the whole system. The value comes from stable note IDs, provenance, status/confidence, links, and retrieval discipline.

## Operations guide

Read the [repository operations guide](docs/operations-guide/README.md) for startup, working checks, troubleshooting, safe shutdown, and the Word/PDF editions.

## Development handbook

Read the [complete project handbook](docs/development-handbook/README.md) for architecture and flow diagrams, local setup, end-user workflows, code and data maps, worked development examples, known gaps, and recovery procedures. Editable Word and formatted PDF editions are included in this repository.
