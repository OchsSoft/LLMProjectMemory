# Using the reference in practice

## A source-backed decision example

Suppose a receiving project's approved architecture says that one durable store owns business records and a search index can be rebuilt. The useful memory is one concise decision describing ownership and its consequence, with a stable ID and a pointer to the accepted architecture or code. It is not an entire chat transcript. If the evidence only shows the search index configuration, the ownership conclusion may be inferred rather than confirmed.

Start by reading the receiving project's instructions and current memory convention. If it already has a canonical system, record or retrieve the decision there using its verified identity and allowed workflow. Study this repository's status, provenance and retrieval ideas without creating a competing vault. If a separate future project explicitly adopts Markdown memory, its maintainers must first define the permitted location, schema parser and review process.

## Construct a pack by hand for understanding

Choose a concrete task such as changing a save format. Find the relevant schema decision, migration constraint and known compatibility issue. Follow only directly useful links. Place confirmed evidence under Canon Facts, hypotheses under Inferred Notes, conflicting records under Disputed Notes, and unresolved compatibility questions under Open Questions. Preserve source pointers in every section. This manual exercise demonstrates the proposed contract without pretending an automated retriever has run.

A small pack should still carry enough context to avoid dangerous ambiguity. “Use the new schema” is unusable without a version and scope. “The version 2 importer accepts version 1 fixtures; tested in this named test at this revision” is reviewable. Conversely, packing every note into context defeats the design's aim and makes conflicting claims harder to see.

## A runtime example, still a design

An application receives a user preference. It first records the event in its own durable store, then proposes a scoped note connected to that event. Validation decides whether the wording and scope are justified. Retrieval can later include the note with its confidence and evidence. If the user corrects the preference, the system should preserve provenance while preventing the older note from silently winning. The repository recommends these separations but does not define correction transactions, deletion behavior or privacy enforcement.

## Finishing a session

There is no process to stop. Save document edits, review `git diff`, and leave a clear local validation result. Do not commit a generated operational vault or raw conversations as an incidental product of reading the skill. If a future implementation produces packs, treat them as derived data unless an explicit audit contract says otherwise; do not accidentally make a stale pack the new source of truth.
