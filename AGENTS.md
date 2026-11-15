# Agent Instructions

These rules apply to every change in G-Commons.

## Before implementation
1. Read this file and the README.
2. Read relevant architecture, standards, and system documents.
3. Inspect existing source, scenes, resources, tests, and call sites before designing.
4. Identify existing APIs and extension points. Extend before duplicating.
5. State assumptions. Do not silently decide project-wide engine, rendering, networking, save-format, or gameplay architecture.

## Implementation rules
- Follow docs/standards/.
- Prefer small cohesive modules and composition over inheritance-heavy frameworks.
- Keep dependencies explicit and one-directional. Avoid circular references and hidden global state.
- Use Nodes for scene-tree behavior, Resources for serializable data, and RefCounted/Object for logic without scene ownership.
- Use typed public APIs where practical.
- Document lifecycle, ownership, dependencies, signals, configuration, and failure behavior.
- Do not add third-party dependencies without documenting purpose, version, license, and removal path.
- Do not silently remove or break public APIs. Include migration notes.
- Avoid speculative abstractions.

## Validation
- Run relevant tests and Godot headless checks when available.
- Never claim a test passed unless it was actually run.
- If validation is unavailable, state that and provide exact commands.

## Completion report
Report behavior delivered, files changed, dependencies/architecture impact, checks actually run, limitations, and migration notes.