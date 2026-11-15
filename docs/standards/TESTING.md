# Testing Standards

Tests protect public contracts, lifecycle behavior, serialization, edge cases, and regressions.

## Layers
1. Unit tests for pure logic and small non-scene components.
2. Scene tests for lifecycle, signals, and composition.
3. Integration tests for module interactions and engine services.
4. Manual acceptance checks for visuals, editor workflows, input, and platform behavior.

## Rules
- Every non-trivial reusable module needs tests or a documented reason tests are impractical.
- Cover normal behavior, invalid inputs, boundaries, and cleanup.
- Avoid order-dependent tests and shared mutable global state.
- Keep fixtures small and representative.
- Record exact engine and runner versions in CI.

No test framework is selected yet. Do not claim automated coverage until a runner and CI are installed and executed.