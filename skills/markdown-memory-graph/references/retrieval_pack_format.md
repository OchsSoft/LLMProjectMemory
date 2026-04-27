# Retrieval Pack Format

A compact retrieval pack should look like:

```md
# Memory Pack

## Canon Facts
- [note-id] Fact text. Source: path/to/source.md

## Inferred Notes
- [note-id] Inferred context. Source: event or note reference

## Disputed Notes
- [note-id] Warning about conflict or uncertainty.

## Open Questions
- [note-id] Question that remains unresolved.
```

Rules:

- Keep packs small.
- Prefer confirmed high-confidence notes.
- Include one-hop linked notes when useful.
- Exclude deprecated notes unless requested.
