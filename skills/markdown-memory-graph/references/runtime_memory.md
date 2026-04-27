# Runtime Memory

Use runtime memory when an application uses LLMs as part of user-facing behavior.

Recommended storage model:

- session_events: raw durable event log
- memory_notes: compact facts, preferences, decisions, world state, or unresolved threads
- memory_links: typed graph edges
- optional embeddings: semantic retrieval aid, not the source of truth

Prompt packs should separate:

- Canon Facts
- Inferred or Unconfirmed Notes
- Disputed Notes
- Recent Events

Do not let narrative generation directly mutate canon without extraction and validation.
