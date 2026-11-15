# G-Commons

G-Commons is a Godot-focused collection of reusable game-development systems, framework modules, architecture guidance, and implementation references.

Its purpose is to provide a consistent foundation for building a game: systems should be reusable, composable, documented, testable, and easy to extend without creating unnecessary dependencies.

## Project status

**Stage:** Foundation / pre-production  
**Engine:** Godot (version to be pinned when selected)  
**Primary language:** GDScript unless a module has a documented reason to use another language.

This repository is being established before the game-specific architecture is finalized. Avoid assuming a particular genre, camera model, networking model, or gameplay loop until those decisions are recorded in `docs/decisions/`.

## Core rules

1. **Inspect before implementing.** Read the relevant module documentation and existing code before adding or changing a system.
2. **Extend before duplicating.** Prefer improving an existing abstraction over creating a competing one.
3. **Keep modules focused.** A system should have a clear responsibility and a small public API.
4. **Use composition.** Prefer scenes, resources, signals, and small cooperating nodes over deep inheritance.
5. **Document contracts.** Public APIs, signals, configuration, lifecycle, dependencies, and failure behavior must be documented.
6. **Make changes testable.** Include automated tests or a reproducible manual test plan.
7. **Preserve Godot conventions.** Use idiomatic GDScript, typed declarations where practical, explicit scene ownership, and stable resource paths.
8. **Avoid speculative frameworks.** Build abstractions in response to concrete needs; do not add layers without a demonstrated benefit.
9. **Keep dependencies explicit.** No hidden autoload assumptions, global state, or circular module dependencies.
10. **Update the knowledge base with the implementation.** Documentation and architecture records are part of every feature.

## Repository map

- `docs/architecture/` — project-wide architecture and module boundaries.
- `docs/standards/` — coding, scene, resource, testing, and documentation conventions.
- `docs/systems/` — system specifications and integration contracts.
- `docs/decisions/` — architecture decision records (ADRs).
- `docs/workflows/` — repeatable implementation, review, and release workflows.
- `addons/g_commons/` — reusable Godot modules intended for reuse.
- `tests/` — automated tests and test fixtures.
- `examples/` — small runnable demonstrations of public APIs.

## Working with ChatGPT or other coding agents

Before making changes:

1. Read `AGENTS.md`.
2. Read the relevant architecture and standards documents.
3. Inspect the existing implementation and tests.
4. Identify the intended extension point and dependencies.
5. Propose a small implementation plan when the change crosses module boundaries.

After making changes:

1. Run the relevant tests and Godot headless validation when available.
2. Update documentation and examples.
3. Record meaningful architectural decisions in `docs/decisions/`.
4. Summarize files changed, behavior added, validation performed, and known limitations.

Never claim a test passed unless it was actually run. Never silently remove an existing public API or feature. Flag breaking changes and migration requirements.

## Initial setup

The Godot project shell, engine version, test runner, and first reusable modules will be established as the project requirements become clear. See `docs/ROADMAP.md` for the bootstrap sequence.
