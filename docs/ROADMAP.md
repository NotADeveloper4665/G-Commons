# G-Commons Bootstrap Roadmap

## Stage 0 — Repository foundation
- [x] Establish purpose and agent instructions.
- [x] Establish architecture and coding standards.
- [ ] Pin the supported Godot 4.x version.
- [ ] Select linting, formatting, and test tooling.
- [ ] Decide whether this is a library-only project, sandbox, or both.

## Stage 1 — Tooling
- Define supported Godot version and compatibility policy.
- Add reproducible local setup instructions.
- Add GDScript linting and formatting.
- Select a compatible test runner and add CI.
- Validate fresh-clone setup and headless import.

## Stage 2 — Reusable foundations
Candidate systems, to be prioritized against actual game requirements:
- Shared resource/configuration patterns.
- Event and signal conventions.
- Scene lifecycle helpers.
- Save/load infrastructure.
- Input and rebinding.
- Debug and developer tooling.

Every module needs a system specification, tests, and a runnable integration example.

## Stage 3 — Game-specific systems
Keep game rules and content in the game layer. Promote a system into G-Commons only when it is genuinely reusable and its game-specific assumptions can be removed.

## Stage 4 — Hardening
Add integration/regression tests, API stability policy, migration docs, and examples for stable modules.

## Priority rule
Reliability and ease of extension outrank the number of systems. Prefer a small set of tested modules over a large framework with unclear ownership.