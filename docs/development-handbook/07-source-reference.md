# Source reference

This handbook describes committed source in OchsSoft/LLMProjectMemory at `c0392ff94c15792c9d693df10f02c9b2ff2d4d29`. Paths below are relative to this repository. Source-defined behavior is distinguished from a fresh runtime verification; no application or game was launched to author these chapters. The existing quick operating guide remains available separately.

## Reading the evidence

A source file explains what the program is designed to do. A test states an expectation and may exercise only one layer. A README describes an intended workflow and can lag implementation. When these disagree, inspect the exact revision and the executable code, reproduce the disagreement in a safe local test, and correct the relevant documentation with the change. Do not treat a passing unit test as proof of rendering, sound, external connectivity, deployment, or save recovery.

## File and symbol index

| File | Responsibility | Entry points and locations |
|---|---|---|
| [README.md](https://github.com/OchsSoft/LLMProjectMemory/blob/c0392ff94c15792c9d693df10f02c9b2ff2d4d29/README.md) | Scope and illustrative note model | L1 to L46 |
| [docs/project-brief.md](https://github.com/OchsSoft/LLMProjectMemory/blob/c0392ff94c15792c9d693df10f02c9b2ff2d4d29/docs/project-brief.md) | Design goals and proposed pipeline | L1 to L81 |
| [docs/example-project-prompts.md](https://github.com/OchsSoft/LLMProjectMemory/blob/c0392ff94c15792c9d693df10f02c9b2ff2d4d29/docs/example-project-prompts.md) | Historical rollout examples | L1 to L19 |
| [skills/markdown-memory-graph/SKILL.md](https://github.com/OchsSoft/LLMProjectMemory/blob/c0392ff94c15792c9d693df10f02c9b2ff2d4d29/skills/markdown-memory-graph/SKILL.md) | Reusable skill specification | L1 to L73 |
| [skills/markdown-memory-graph/references/note_schema.md](https://github.com/OchsSoft/LLMProjectMemory/blob/c0392ff94c15792c9d693df10f02c9b2ff2d4d29/skills/markdown-memory-graph/references/note_schema.md) | Frontmatter fields and meaning | L1 to L23 |
| [skills/markdown-memory-graph/references/retrieval_pack_format.md](https://github.com/OchsSoft/LLMProjectMemory/blob/c0392ff94c15792c9d693df10f02c9b2ff2d4d29/skills/markdown-memory-graph/references/retrieval_pack_format.md) | Output sections and selection guidance | L1 to L26 |
| [skills/markdown-memory-graph/references/build_time_memory.md](https://github.com/OchsSoft/LLMProjectMemory/blob/c0392ff94c15792c9d693df10f02c9b2ff2d4d29/skills/markdown-memory-graph/references/build_time_memory.md) | Development knowledge scope | L1 to L16 |
| [skills/markdown-memory-graph/references/runtime_memory.md](https://github.com/OchsSoft/LLMProjectMemory/blob/c0392ff94c15792c9d693df10f02c9b2ff2d4d29/skills/markdown-memory-graph/references/runtime_memory.md) | Proposed runtime records and canon validation | L1 to L19 |

## Keeping the handbook useful

When code changes, update the chapter that explains its contract, the relevant diagram, the change recipe, and this pinned source register. Keep the Word and PDF editions synchronized with the Markdown chapters. Record what was actually tested, what remained unverified, and which saved data must survive an upgrade. A future maintainer should be able to trace an instruction to a file or a test without relying on a previous conversation.
