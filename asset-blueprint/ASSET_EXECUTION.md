# Asset Execution

## Purpose

Asset Execution translates an approved Asset Blueprint into task-specific instructions for image generation, retouching, image editing, image-to-video and multi-shot video continuity.

An Asset Blueprint is not a complete generation prompt. The [Creative Workflow](../CREATIVE_WORKFLOW.md) remains authoritative for Project Definition, world logic, physics, materials, lighting, camera, composition, commercial intent and Scene Locks.

## Execution Data Layers

Use these layers:

1. Asset Blueprint
2. Selected Variant
3. Current Temporary State
4. Project Definition
5. Scene Locks
6. Shot-specific Instructions
7. Tool or Model Constraints

Do not paste the complete Blueprint into every prompt. Translate only the required information into a **Task-specific Execution Package**.

## Task-Specific Execution Package

### Task Context

- Objective
- Deliverable
- Platform and format
- Blueprint Level
- Tool or Model Constraints

### Active Asset

- Asset name
- Asset Version
- Blueprint status
- Selected Controlled Variation
- Current Temporary State

### Identity Requirements

- Permanent Asset Locks
- Recognition Anchors
- Required silhouette and proportion relationships
- Required colours, materials, logos or markings

### Allowed Changes

- Permitted Variation
- Controlled Variation scope
- Temporary State Changes
- Elements requiring approval before change

### Active Reference Package

- Primary source for each required Reference Role
- Approved Scope
- Excluded Signals
- Diagnostic References kept separate

### Scene Integration

- Project Definition
- Scene Locks
- Contact, support, occlusion and scale
- Environmental and material response

### Shot Instructions

- Camera and composition
- Action or interaction
- Start and end condition
- Shot-specific exclusions

### Continuity Requirements

- Previous state
- Required current state
- Required next state
- Screen direction, orientation and scale

### Known Risks

- Known Failure Modes
- Single-view limitations
- Tool or model risks
- Unresolved conflicts

### Validation Targets

- Global Validation targets
- Asset Validation gates
- Output size and crop requirements

### Execution Decision

- Generate
- Retouch
- Regenerate
- Request clarification
- Replan references, Blueprint, shot or tool strategy

## Prompt Translation

Translate approved source information into:

- **Identity Anchor** — concise approved identity and Recognition Anchors.
- **Structural Anchor** — silhouette, proportions, topology and connection logic needed for the task.
- **Integrity Anchor** — identity elements that must not drift, disappear, merge, multiply or change category.
- **Current Variant and State** — approved Controlled Variation and Temporary State Changes.
- **Scene and Physical Interaction** — support, contact, pressure, moisture, heat, occlusion and environmental response.
- **Camera and Composition** — selected view, lens behaviour, framing and hierarchy.
- **Lighting and Material Response** — intrinsic materials translated through current scene lighting.
- **Action or Motion** — movement, articulation, timing and start/end state.
- **Consistency Safeguards** — Known Failure Modes and validation-critical constraints.
- **Exclusions** — unrelated signals and prohibited interpretations.

Prompt Anchors are execution outputs, not the source of truth. Approved Blueprint Locks and References remain authoritative.

## Image Generation

Load Blueprint → select Controlled Variation and Temporary State → build Task-specific Reference Package → apply Project Definition → define Scene Locks → define Camera and Composition → create Task-specific Execution Package → generate → Global Validation → Asset Validation.

Generated output does not become new Blueprint authority. New visible content is Observed until explicitly approved.

## Image Retouching

### Preserve

- All correct existing elements
- Unrelated Permanent Asset Locks
- Unrelated Scene Locks
- Approved composition and world logic

### Correct

- Only required identity, structural, material, logo, perspective or continuity errors

### Reconcile

- Shadows
- Reflections
- Contact
- Occlusion
- Moisture
- Pressure
- Perspective
- Secondary physical effects

### Validate

- Global world first
- Asset identity second

Do not reconstruct the complete scene unless required.

## Video and Multi-Shot Execution

Asset Blueprint → Sequence Continuity Sheet → Shot List → Per-shot Execution Package → Keyframe Generation → Image-to-Video → Shot Validation → Sequence Validation.

### Sequence Continuity Format

- Sequence ID
- Active Asset and Blueprint Version
- Controlled Variation
- Initial Temporary State
- Required final state
- Location and environment
- Overall screen direction
- Sequence-level Scene Locks
- Continuity risks

### Shot Execution Format

- Shot ID
- Shot objective
- Blueprint Version
- Controlled Variation
- Temporary State
- Active Reference Package
- Camera and composition
- Action and Motion Complexity Level
- Location and orientation
- Costume and props
- Damage and wetness
- Scale and lighting
- Entry and exit direction
- Global and Asset Validation targets

### Shot End State

- Asset identity state
- Position and orientation
- Costume and props
- Damage and wetness
- Opened or closed components
- Scale
- Lighting condition
- Screen direction
- Dependencies for the next shot

Track Blueprint Version, Variant, Temporary State, location, orientation, costume, props, damage, wetness, scale, lighting, screen direction, and entry and exit direction for every shot.

## Motion Complexity

### Level 1 — Minimal Motion

- Breathing
- Blinking
- Slight head movement
- Subtle fabric movement
- Slow camera push

### Level 2 — Controlled Motion

- One step
- Raising an arm
- Small turn
- Picking up one object
- Simple sitting action

### Level 3 — Complex Motion

- Running
- Jumping
- Full-body rotation
- Intense interaction
- Two-character physical contact

Split Level 3 into multiple shots where identity risk is high.

### Level 4 — Multi-event Motion

- Several causal actions in one shot
- Attack, impact, fall and recovery
- Complex exchanges
- Transformation sequences

Level 4 should normally be divided into multiple shots unless there is a deliberate and validated reason not to do so.

Motion Complexity does not change Blueprint Level or Asset Version.

## Tool-Neutral Execution

Keep the Blueprint independent of any specific commercial platform.

### Text-to-Image

Emphasise concise Identity, Structural and Integrity Anchors, a minimum sufficient Task-specific Reference Package and clear exclusions.

### Image-to-Image

Separate source identity from source pose, scene, camera, lighting and style. Control transformation strength through the chosen tool without changing Blueprint authority.

### Image Editing

Preserve correct pixels and relationships. Localise the change and reconcile secondary physical effects.

### Image-to-Video

Emphasise start-frame identity, Shot End State, Motion Complexity, temporal drift risks and sequence continuity.

### Dedicated Character Model or LoRA

Treat the model as an execution tool, not as identity authority. Validate its learned behaviour against the approved Blueprint and references. Do not add training specifications to this module.
