# Architecture Overview

This is an initial architecture contract, not a claim that all modules already exist. Game-specific decisions remain open until requirements are recorded.

## Conceptual layers
1. Engine integration: thin adapters around Godot APIs where useful.
2. Reusable foundations: engine-aware but game-agnostic modules under addons/g_commons/.
3. Game systems: mechanics and rules specific to the game; normally live in the game repository.
4. Presentation and composition: scenes, UI, animation, audio, and orchestration.

Reusable foundations must not depend on game-specific scenes, entities, balance values, or story content.

## Godot principles
- Prefer Nodes for behavior with a scene-tree lifecycle.
- Prefer Resources for serializable data and configuration.
- Prefer RefCounted or lightweight Objects for logic without scene ownership.
- Prefer composition, exported references, and explicit setup over global lookups.
- Use Autoloads only for genuinely application-wide services with documented lifecycle and ownership.
- Use signals for observable events; document emitters, consumers, and payloads.
- Keep scenes and scripts close to the feature they implement.

## Module contract
Every reusable module defines its responsibility, non-goals, public API, dependencies, lifecycle/ownership, configuration, signals, failure behavior, tests, and usage example.

## Unresolved decisions
Do not guess: exact Godot version, 2D/3D/mixed needs, renderer/target hardware, networking model, save compatibility, input/accessibility requirements, and whether the package ships as an addon or source library.