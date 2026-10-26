# Gaps, diagnosis and recovery

## Current limitations and next steps

| Priority | Gap and affected material | Observable acceptance |
|---|---|---|
| First | Illustrative frontmatter may parse links inconsistently; README, skill, note schema | One specified representation, valid/invalid fixtures and deterministic parser behavior |
| First | No executable validator or retrieval compiler | Explicit toolchain, local checks and documented invocation; no undocumented background service |
| First | No access-control or correction protocol for runtime use | Scoped scenarios demonstrate permitted reads and validated corrections without canon contamination |
| Next | Retrieval budget/order/conflict rules are qualitative | Stable fixture packs cover truncation, ties, cycles, disputes and deprecated records |
| Next | No schema versions or migration contract | Old fixtures migrate or fail clearly with retained original evidence |
| Later | No embedding/index implementation | Index rebuild proves original records and provenance remain canonical |

## Troubleshooting without inventing a runtime

| Symptom | Evidence to inspect | Safe response |
|---|---|---|
| There is no start command | Tracked file list and absence of package manifest | Use the design documents; do not invent a server invocation |
| A parser rejects an example | Exact YAML bytes and chosen parser version | Preserve original example, isolate a minimal fixture and standardize syntax |
| A pack says an inference is a fact | Note status and pack section | Correct section routing and test the case before relying on the pack |
| Old information keeps returning | Status, source revision and index policy | Resolve supersession explicitly; rebuild only derived retrieval data |
| A rollout prompt conflicts with project rules | Receiving repository instructions and current authority | Follow the receiving project's rules; amend the reusable example if misleading |
| Links lead nowhere | Stable IDs versus filenames and relative paths | Repair references deliberately; do not create duplicate identities casually |

## Preservation and recovery

The committed Markdown and Git history are the repository's authoritative artifacts. Back up the repository with its history and any explicitly adopted external evidence separately. A document export is useful for reading but cannot replace editable contracts and source links. There are no database volumes, user accounts or running sessions to back up here.

Before undoing a document change, compare the exact diff and preserve unrelated work. Recover a specific known revision into a separate file or clean checkout for comparison instead of resetting an active working tree. If a future application adopts this pattern, its event store needs its own tested backup and restore procedure; copying this reference repository cannot restore that application's memory.

A successful recovery means the relevant source can be read, metadata meaning is consistent, links resolve, and no unsupported claim has been elevated to accepted truth. It does not mean an unimplemented runtime has become operational.
