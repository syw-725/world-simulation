# Asset Blueprint

Asset Blueprint is an optional YCOS module for maintaining the identity and continuity of reusable visual assets across images, camera angles, scenes, styles and video shots.

It can be used for characters, products, objects, creatures, mascots, vehicles, mecha, environments and other reusable visual assets.

Asset Blueprint does not replace the root [Creative Workflow](../CREATIVE_WORKFLOW.md) or [Validation](../VALIDATION.md). The Creative Workflow remains authoritative for project understanding, world definition, physics, materials, object interaction, lighting, camera, perspective, composition, commercial intent and scene logic. Root YCOS validation remains mandatory and runs before asset-specific validation.

## Activation Levels

- **Level 0 — No Blueprint:** Continue through the existing YCOS workflow unchanged.
- **Level 1 — Lightweight Blueprint:** Use for limited or medium-risk consistency.
- **Level 2 — Full Blueprint:** Use for persistent, multi-angle, multi-scene, video, brand, product, IP or high-risk continuity.

The Full Blueprint extends the Lightweight Blueprint. It does not use a separate or incompatible format.

The Asset Consistency Decision occurs after Project Understanding / Project Definition and before detailed execution. The Blueprint may inform later world, camera, scene and execution decisions, but it does not replace them.

## Module Documents

- [Asset Blueprint Protocol](ASSET_BLUEPRINT_PROTOCOL.md) defines activation, intake, authority, references, locks and change classification.
- [Asset Blueprint Template](ASSET_BLUEPRINT_TEMPLATE.md) defines the Lightweight and Full Blueprint structures.
- [Asset Execution](ASSET_EXECUTION.md) translates an active Blueprint into task-specific execution.
- [Asset Validation](ASSET_VALIDATION.md) extends root YCOS validation with asset continuity checks.
- [Asset Lifecycle](ASSET_LIFECYCLE.md) defines lifecycle states, versioning and change control.

## Boundaries

This module is AI-model agnostic. It defines creative reasoning and continuity controls, not model-specific prompt syntax.

It does not establish an asset library, generate sample assets, store reference images, create tool adapters, provide prompt libraries, define machine-readable schemas or introduce scripts or dependencies.

