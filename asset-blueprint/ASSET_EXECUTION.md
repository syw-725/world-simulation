# Asset Execution

## Purpose

Asset execution translates an Active or Locked Asset Blueprint into instructions for a specific image, retouch or video task.

An Asset Blueprint is not a complete generation prompt. It defines reusable identity and continuity requirements. The root [Creative Workflow](../CREATIVE_WORKFLOW.md) remains authoritative for the project world, physics, materials, object interaction, lighting, camera, perspective, composition, commercial intent and scene logic.

Execution remains AI-model agnostic. Tool or model constraints may affect implementation strategy but do not redefine asset identity.

## Execution Package

Create a task-specific Execution Package from:

1. **Asset Blueprint** — the applicable Active or Locked identity definition and Asset Version.
2. **Selected Variant** — the approved Controlled Variation, if any.
3. **Temporary State** — the shot-, scene- or sequence-specific condition.
4. **Project Definition** — objective, audience, deliverable, format, commercial intent and constraints.
5. **Scene Locks** — environment, camera, lighting, composition, perspective, hero placement and other locked scene decisions.
6. **Shot-specific Instructions** — action, framing, interaction, timing and intended change for the current output.
7. **Tool / Model Constraints** — relevant capabilities, limitations, input requirements and continuity risks.

The Execution Package must also include the task-specific Reference Package, unresolved conflicts, required validation level and known failure modes relevant to the task.

## Execution Anchors

### Identity Anchor

A compact model-neutral statement of who or what the asset is and which recognition anchors must remain identifiable.

### Structural Anchor

A compact model-neutral statement of silhouette, proportions, construction, topology and component relationships required by the current view or action.

### Integrity Anchor

A compact model-neutral statement of what must not drift, merge, disappear, multiply, change category or be mistaken for a Temporary State.

The three anchors are selected from approved Blueprint content. They do not replace the complete Blueprint, Project Definition, Scene Locks or physical reasoning.

## Translation Process

1. Confirm activation level, Asset Version and lifecycle state.
2. Select the Controlled Variation, if applicable.
3. Declare the Temporary State and its scope.
4. Select a task-specific Reference Package.
5. Load Project Definition and Scene Locks.
6. Detect conflicts between identity, scene and shot requirements.
7. Classify each requested asset change using the four-way change classification.
8. Build the Identity, Structural and Integrity Anchors.
9. Adapt the asset to the world, camera and shot without redesigning intrinsic identity.
10. Execute using the relevant tool or model constraints.
11. Run root YCOS validation first, followed by [Asset Validation](ASSET_VALIDATION.md).

## Domain-Safe Translation

Permanent Asset Locks and Scene Locks govern separate domains and must not silently overwrite each other.

- Preserve approved intrinsic identity while allowing physically correct lighting, reflection, atmospheric, occlusion and camera effects.
- Preserve authoritative Scene Locks while selecting views, poses and interactions that maintain recognition.
- Treat scene-dependent visible changes as adaptations or Temporary States, not canonical identity changes.
- When coexistence is impossible, stop silent execution and follow the conflict process in the [Asset Blueprint Protocol](ASSET_BLUEPRINT_PROTOCOL.md).

## Image-Generation Workflow

1. Complete Project Understanding and the Asset Consistency Decision.
2. Establish the applicable world and scene logic through the root Creative Workflow.
3. Build the Execution Package and Reference Package.
4. Define the three Execution Anchors.
5. Translate canonical identity into the selected camera, perspective, lighting, composition and style.
6. Generate without promoting incidental output details into the Blueprint.
7. Run root YCOS validation.
8. Run asset validation and apply the resulting action.

Generated details are output evidence only. They remain Observed until deliberately confirmed and must not become Permanent Asset Locks automatically.

## Image-Retouch Workflow

1. Diagnose the image using the root Creative Workflow.
2. Use Diagnostic References to identify drift or undesirable outcomes without treating them as positive identity sources.
3. Identify the exact identity, scene or local defect.
4. Build a focused Execution Package that locks unrelated content.
5. Preserve Scene Locks and unaffected Permanent Asset Locks.
6. Retouch the minimum required region while updating physically necessary secondary effects.
7. Run root retouch validation first.
8. Run asset validation to confirm identity and state continuity.

A local identity correction must not redesign the scene. A scene correction must not silently redesign the asset.

## Video and Multi-Shot Workflow

1. Define the project, sequence purpose and continuity risk.
2. Select the Asset Version and Controlled Variation for the sequence.
3. Define the initial Temporary State and permitted state progression.
4. Assign Motion Complexity Level 1–4.
5. Create a Sequence Continuity Sheet.
6. Create a separate Execution Package for every shot.
7. Select task-specific Reference Packages for each shot.
8. Validate each shot against the Blueprint, previous approved shot and intended state progression.
9. Validate the complete sequence for temporal, identity, motion and commercial continuity.

## Sequence Continuity Sheet

The Sequence Continuity Sheet records, per shot:

- Shot identifier and order
- Asset Version
- Selected Controlled Variant
- Entry and exit Temporary State
- Required identity, structural and integrity anchors
- Camera, action and interaction
- Motion Complexity Level
- Scene Locks and permitted scene changes
- Reference Package
- Continuity dependencies from previous and following shots
- Validation result, severity and required correction

The sheet is a project continuity record. It is not an Asset Version, Controlled Variant, Temporary State or substitute Blueprint.

## Per-Shot Execution Package

Every shot receives its own Execution Package. It must preserve sequence-level decisions while containing only the references and instructions needed for that shot.

If a shot requires a different Controlled Variation or a change to Permanent Asset Locks, classify and approve that change before execution. Do not conceal an identity revision as shot-specific adaptation.

## Motion Complexity Levels

### Level 1 — Minimal Motion

Small movement with limited deformation, articulation, viewpoint change or occlusion. Examples of complexity include subtle expression, breathing, small product motion or a simple camera hold.

### Level 2 — Controlled Motion

Moderate pose, articulation, interaction or camera movement with predictable continuity and limited occlusion.

### Level 3 — Complex Motion

Large articulation, rapid action, substantial camera change, interaction, deformation, occlusion or view translation requiring stronger per-shot structural control.

### Level 4 — Multi-event Motion

A shot containing multiple sequential actions, state changes, exchanges or cause-and-effect events. Examples include attack, impact, fall and recovery in one shot; multiple object exchanges; transformation followed by action; or several narrative events within one generation.

Level 4 should normally be decomposed into multiple shots unless there is a deliberate and validated reason not to do so.

Motion Complexity Level describes execution risk. It does not change the Blueprint activation level or Asset Version.

## Model-Neutral Execution Principles

- Express identity through approved semantic and structural anchors rather than model-specific syntax.
- Adapt package detail to tool capabilities without changing source authority.
- Use the smallest Reference Package that covers the task.
- Treat generated outputs as results to validate, not new canonical sources.
- Prefer controlled retouch when drift is local and regeneration when structure is broadly wrong.
- Replan at S4 rather than repeating the same failed strategy.
- Preserve commercial readability as well as continuity.
