# Implementation Workflow

1. Clarify behavior, constraints, acceptance criteria, and non-goals.
2. Inspect existing code, scenes, resources, tests, and docs.
3. Map affected modules, APIs, dependencies, ownership, lifecycle, and migration risks.
4. Write/update a system specification; record cross-cutting decisions as ADRs.
5. Plan small, independently verifiable steps.
6. Implement using established patterns; avoid unrelated refactors.
7. Validate headless import, static checks, tests, and manual acceptance as applicable.
8. Update docs, API references, examples, and changelog.
9. Review for coupling, regressions, dead code, and failure paths.
10. Report exactly what changed and what validation ran.

Stop and ask before breaking public APIs, adding substantial dependencies, changing save formats, introducing global state/Autoloads, or locking project-wide architecture.