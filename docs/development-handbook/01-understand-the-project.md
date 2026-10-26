# Understand the project

## What this repository delivers

LLMProjectMemory is a design reference and a reusable skill specification for portable, linked project knowledge. It is not a running memory server, database package, command line program or search engine. The committed implementation consists of Markdown documents and a skill directory. There is no dependency manifest, executable retrieval compiler, parser, database migration or automated test suite in this baseline.

Think of its proposed memory graph as a box of small index cards. Each card says one useful thing, names the evidence behind it, says whether it is known or inferred, and points to related cards. A retrieval pack is a deliberately small selection of those cards for a particular task. This is intended to avoid repeatedly reading an entire project or mistaking an old conversation for present authority.

The important distinction is between a pattern and a product. The schema in `references/note_schema.md` describes what an implementation should accept. The retrieval document describes the format a compiler should produce. Neither document proves that a compiler exists. An operator can study or adapt this material, but cannot start a background service from this repository.

## Two uses, with different ownership

Build-time memory helps a developer or coding assistant understand architecture, constraints, domain rules, migrations and known problems. The application being developed need not use AI. Runtime memory belongs to an application whose user-facing behavior uses an LLM. Runtime memory needs durable application storage, explicit scopes and validated state changes; the skill specifically recommends that Markdown should not be the runtime source of truth.

A hybrid project might use both, but the two must not become one unfiltered transcript archive. A developer preference is not automatically a customer preference. A generated story is not automatically an accepted domain fact. A confidence label is a statement about evidence, not a permission to act.

## Workspace boundary

The workspace currently uses a canonical durable project memory system and forbids ad hoc operational memory files. The skill's example instruction to create `docs/llm-memory/` is therefore a reusable proposal, not authorization to create parallel operational vaults in existing workspace projects. Follow the receiving project's governing instructions first. This handbook adds ordinary project documentation; it does not adopt a new canonical store.

The project has no supplied canonical project key in the workspace list. Do not infer a key from the repository name. Any future integration requiring an exact identity must first resolve that identity explicitly.

## Read in this order

Read `README.md` for scope, `docs/project-brief.md` for the intended pipeline, then the skill and its four references for contracts. `docs/example-project-prompts.md` preserves initial rollout prompts. Treat those prompts as historical examples and proposed work, not evidence that their target projects now implement every requirement. This chapter and the architecture chapter explain how to review those requirements independently.
