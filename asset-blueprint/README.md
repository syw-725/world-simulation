# Asset Blueprint

Asset Blueprint is an optional consistency-control layer under the YCOS [Creative Workflow](../CREATIVE_WORKFLOW.md). It defines what a persistent visual asset is and how its approved identity remains consistent across images, angles, scenes, lighting conditions, styles, sequences, image-to-video work and future projects.

It supports recurring characters, creatures, mascots, products, objects, vehicles, mecha, environments, food assets and other persistent visual assets.

Asset Blueprint is not a replacement for Project Definition, Creative Intent, world simulation, physics, materials, lighting, camera, composition, Scene Locks, commercial judgement or [Global Validation](../VALIDATION.md). It is not an asset library, model adapter, prompt library or automatic visual-board generator.

## Conceptual Boundaries

- **Asset Blueprint** defines what the asset is and how its identity remains consistent.
- **Creative Workflow** defines the believable and commercially effective world in which the asset appears.
- **Scene Locks** define the current project world.
- **Permanent Asset Locks** define persistent asset identity.

Scene Locks and Permanent Asset Locks govern different domains. Neither silently overwrites the other.

## When to Activate

Make the optional Asset Consistency Decision after Project Understanding and before detailed execution.

- **Level 0 — No Blueprint:** One-off exploration, mood testing, generic non-recurring elements or no persistent identity requirement. Continue through YCOS unchanged.
- **Level 1 — Lightweight Blueprint:** Limited reuse, several images, basic angle changes, a short-term project or medium consistency risk.
- **Level 2 — Full Blueprint:** Persistent IP, brand-sensitive assets, multi-angle or multi-scene work, image sequences, video, image-to-video, cross-model use, long-term reuse or high identity and structural risk.

The required level should be proportional to reuse frequency, consistency requirements, structural complexity and generation failure risk. Level 2 extends Level 1 rather than replacing it with another format.

## Text-First Default

`Build | Asset Blueprint` defaults to a text-based Draft Blueprint. Do not generate a character sheet, turnaround, infographic, presentation board, comparison board, redesigned asset, new angle or new asset image unless the user explicitly requests visual generation.

The text Blueprint remains authoritative over any generated visual Blueprint sheet.

## Documents

1. [ASSET_BLUEPRINT_PROTOCOL.md](ASSET_BLUEPRINT_PROTOCOL.md) — authoritative activation, intake, evidence, reference, lock and review rules.
2. [ASSET_BLUEPRINT_TEMPLATE.md](ASSET_BLUEPRINT_TEMPLATE.md) — reusable Lightweight Blueprint and Full Blueprint format.
3. [ASSET_EXECUTION.md](ASSET_EXECUTION.md) — translation from an approved Blueprint into task-specific image, retouch and video instructions.
4. [ASSET_VALIDATION.md](ASSET_VALIDATION.md) — asset-specific validation after mandatory Global Validation.
5. [ASSET_LIFECYCLE.md](ASSET_LIFECYCLE.md) — lifecycle status, versioning, compatibility and GitHub storage principles.

## Scope Exclusions

This module is AI-model agnostic. It does not create assets, examples, reference images, tool adapters, prompt or shot libraries, JSON schemas, databases, automation scripts, binary images, video files, LoRA training specifications or actual Blueprint records.
