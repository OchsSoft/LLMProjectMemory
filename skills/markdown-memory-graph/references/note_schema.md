# Note Schema

Required frontmatter fields:

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

Guidelines:

- Keep one concept per note.
- Write enough local context that the note is meaningful alone.
- Preserve provenance.
- Never store speculation as confirmed truth.
- Prefer stable note IDs over title-derived links when possible.
