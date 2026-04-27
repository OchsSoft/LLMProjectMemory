# Example Project Prompts

These prompts came from the initial planning thread and should eventually become examples/tests for the reusable skill.

## GoingDutch

Implement build-time LLM memory only. Do not add AI features to the app runtime. Seed `docs/llm-memory/` from AGENTS.md, CLAUDE.md, docs, `.codex`, and `.claude/rules`, especially migration policy, Drizzle/PostGIS/Redis gotchas, Expo constraints, testing workflow, branch/security policy, and subscription/organization lifecycle docs.

## DungeonMind

Implement durable runtime memory for in-app AI continuity. Add session events, memory notes, memory links, retrieval packs, and StoryEngine context injection. Keep confirmed facts separate from inferred notes. Do not implement vector embeddings in the first phase unless already supported.

## PyGames

Implement lightweight build-time memory. Preserve framework decisions, Linux compatibility requirements, controller/input architecture, local multiplayer assumptions, porting strategy, and packaging constraints. Do not modify game behavior.

## RouteSweet

Convert HANDOFF.md and README.md knowledge into an Obsidian-style build-time memory vault. Preserve confirmed Blizzard API findings, tested features, in-game test commands, open live-data TODOs, user preferences, release workflow, addon architecture, and chat command length constraints. Do not modify Lua addon behavior in the first pass.
