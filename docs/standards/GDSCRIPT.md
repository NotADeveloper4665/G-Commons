# GDScript Standards

- Use snake_case for files, functions, variables, and signals.
- Use PascalCase for classes and named types.
- Use UPPER_SNAKE_CASE for constants where appropriate.
- Prefer one primary responsibility per script.
- Use class_name only for types intended as reusable public API.
- Add static types to public APIs and important state.
- Keep functions focused; avoid deeply nested control flow.
- Use exported properties for designer-facing configuration, with ranges/tooltips where useful.
- Avoid magic numbers and undocumented warning suppression.

## Godot-specific
- Use lifecycle callbacks only when their semantics are needed.
- Avoid expensive work in per-frame callbacks.
- Prefer signals or explicit method calls over polling.
- Cache node references where appropriate; avoid fragile absolute paths.
- Use preload for fixed dependencies and load for genuinely dynamic paths.
- Validate externally supplied NodePaths, resources, and persisted data.
- Do not use Autoloads as dumping grounds.

## Documentation
Explain intent and constraints, not obvious syntax. Document public methods, signals, exported configuration, and lifecycle assumptions.