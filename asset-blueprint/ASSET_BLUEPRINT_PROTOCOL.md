# Asset Blueprint Protocol

## Purpose and Scope

Asset Blueprint is an optional consistency-control layer under the [Creative Workflow](../CREATIVE_WORKFLOW.md) used to define, protect and reuse the identity, structure, proportions, materials, colours, behaviour and cross-angle or cross-scene translation rules of persistent visual assets.

It may be used for recurring characters, creatures, mascots, products, objects, vehicles, mecha, environments, food assets and other persistent visual assets.

It does not replace:

- Project Definition
- Creative Intent
- World Simulation
- Physical Logic
- Material Behaviour
- Lighting
- Camera
- Composition
- Scene Locks
- Global commercial judgement
- [Global Validation](../VALIDATION.md)

Asset Blueprint determines whether the subject remains the same approved asset. Creative Workflow determines whether that asset exists in a believable and commercially effective visual world.

## Activation Levels

### Level 0 — No Blueprint

Use for:

- One-off exploration
- Mood testing
- Generic non-recurring elements
- Work with no persistent identity requirement

Level 0 continues through the existing YCOS workflow unchanged.

### Level 1 — Lightweight Blueprint

Use for:

- Limited reuse
- Several images
- Basic angle changes
- Short-term projects
- Medium consistency risk

Complete the Lightweight Blueprint sections of the [template](ASSET_BLUEPRINT_TEMPLATE.md).

### Level 2 — Full Blueprint

Use for:

- Persistent IP
- Brand-sensitive assets
- Multi-angle work
- Multi-scene work
- Image sequences
- Video and image-to-video
- Cross-model use
- Long-term reuse
- High identity or structural risk

Level 2 extends the same Level 1 format with the Full Blueprint sections.

The required Blueprint level should be proportional to reuse frequency, consistency requirements, structural complexity and generation failure risk. Asset Blueprint remains optional and does not create another YCOS mode or Bootstrap sequence.

## Text-First Governance

When the user requests `Build | Asset Blueprint`, default to a text-based Draft Blueprint.

Do not immediately generate:

- A visual character sheet or turnaround sheet
- An infographic, presentation board or comparison board
- A redesigned asset
- New viewing angles
- A new character, product or object image

Visual generation is permitted only when the user explicitly requests direct generation, a visual Blueprint sheet, additional angles, turnaround views, character or object sheet artwork, or approved Blueprint visualisation.

If the user says not to generate yet, stop after the text Draft and review requirements.

The required first response contains only:

- Build Mode status
- Project Definition
- Recommended Blueprint Level
- Asset Intake Record
- Reference Role Separation
- Evidence Classification
- Proposed Permanent Asset Locks
- Proposed Controlled Variations
- Known Failure Risks
- Open Decisions
- Review Questions

Do not display private chain-of-thought.

## Asset Intake

Support:

- Text-led Intake
- Image-led Intake
- Multi-image Intake
- Hybrid Intake
- Existing generated asset Intake
- Existing Blueprint Revision

Incomplete input is acceptable. Do not assume that a complete three-dimensional character, product or object specification exists.

The Intake process is:

1. **Intake classification** — identify the input type, intended use and expected continuity risk.
2. **Reference Separation** — give every source a Reference Role, authority and Approved Scope.
3. **Observable extraction** — record what is explicitly stated or directly visible without adding assumptions.
4. **Uncertainty mapping** — identify Undefined, Inferred and Conflicted information.
5. **Draft Blueprint creation** — organise the available evidence without treating it as approved identity.
6. **User review** — confirm, correct, reject or request evidence.
7. **Active or Locked approval** — activate reviewed content or formally approve Permanent Asset Locks.

## Reference Separation

Possible Reference Roles are:

- Identity
- Facial Identity
- Silhouette
- Structure
- Proportion
- Angle
- Material
- Colour
- Logo or Marking
- Costume or Accessory
- Pose
- Interaction
- Motion
- Camera
- Lighting
- Environment
- Style
- Diagnostic Failure Reference

Every reference entry records:

- Reference ID
- Source
- Reference Role
- Source Authority
- Approved Scope
- Excluded Signals
- Confidence
- Known Limitations
- Notes

A reference image is never an instruction to copy every visible signal. Background, pose, lighting, camera, composition, environment, Temporary State Changes and style do not become permanent asset identity unless explicitly approved.

## Evidence Classification

Use exactly these classifications:

### Confirmed

- Explicitly stated or approved by the user
- Or already approved in an Active or Locked Blueprint

### Observed

- Clearly visible in a supplied reference
- Not yet explicitly approved

### Inferred

- A reasonable deduction
- Not directly visible or confirmed

### Proposed

- A design recommendation or completion suggested by the system

### Undefined

- Insufficient information

### Conflicted

- Two or more sources provide incompatible information

Visible image content alone is Observed, not Confirmed. Observed, Inferred, Proposed, Undefined and Conflicted information must not automatically become Permanent Asset Locks.

## Source Authority

Use this hierarchy within each source's authorised scope:

1. User's latest explicit instruction
2. Locked Asset Blueprint
3. User-approved Permanent Asset Locks
4. Approved Primary Reference within its authorised scope
5. Confirmed Active Blueprint content
6. Secondary Reference within its authorised scope
7. Contextual Reference
8. Observed information
9. Inferred information
10. Proposed information

Do not average, merge or creatively combine conflicting identity information without approval. Unresolved differences must be marked **Pending Confirmation**.

Authority is scoped. A Primary pose reference does not overwrite identity, colour, material, costume or structure unless those signals are in its Approved Scope.

## Conflict Resolution

Classify conflicts as:

- **Direct Conflict** — sources disagree within the same approved domain.
- **Version Conflict** — sources represent different asset versions.
- **Perspective Conflict** — viewpoint or lens effects appear to change structure.
- **Style Conflict** — style translation appears to change identity.
- **Artifact Conflict** — a suspected error appears as a design feature.

Use this process:

Detect conflict → classify conflict → check Source Authority → check existing Permanent Asset Locks → determine whether the difference is an intentional variation, perspective effect, style translation, version change or AI artifact → resolve or mark Pending Confirmation → update Blueprint status where appropriate.

Possible outcomes are:

- Resolved
- Pending Confirmation
- Preserved as Variation

## Asset Locks and Change Classes

### 1. Permanent Asset Locks

Permanent Asset Locks may include:

- Core identity
- Silhouette
- Proportions
- Structure
- Intrinsic colours
- Intrinsic materials
- Logo and markings
- Required accessories
- Facial identity
- Packaging form
- Mechanical construction

A feature becomes a Permanent Asset Lock only when explicitly required by the user, explicitly approved during review, or already present in an Active or Locked Blueprint.

### 2. Controlled Variations

Controlled Variations:

- Must be explicitly approved
- Remain within the same Asset Version
- Define changed and unchanged elements
- Must not be silently invented

When no variation is approved, state: **No Controlled Variations approved yet.**

### 3. Temporary State Changes

Temporary State Changes may include wetness, dirt, damage, opening or closing, food preparation state, held props, temporary costume, environmental colour cast and motion deformation.

Temporary State Changes remain separate from permanent identity.

### 4. New Version or Redesign

Changes to core silhouette, proportions, structure, primary colour system, logo, facial design or required accessories require a new major Asset Version or redesign review.

## Asset Locks and Scene Locks

Permanent Asset Locks and Scene Locks govern different domains.

- Permanent Asset Locks govern approved persistent asset identity.
- Scene Locks govern the current project world, including environment, camera, lighting, perspective, composition and hero placement.

Neither silently overwrites the other. Detect genuine conflicts, classify the requested difference and preserve both approved authorities where possible. Request clarification or create a deliberate major Asset Version when they cannot coexist.

## Material and Lighting Separation

Separate intrinsic material identity from temporary lighting appearance.

- Preserve transparent amber plastic; do not preserve exact highlight intensity.
- Preserve matte fabric; do not preserve the current shadow direction.
- Preserve metallic material identity; do not preserve reflected environmental colours as intrinsic colour.

Do not exclude a material when the user explicitly requires it to remain. Exclude only temporary lighting, reflections, colour casts and environmental appearance where appropriate.

## Single-View Limitation

When only one reference angle exists:

- Do not claim complete three-dimensional knowledge.
- Do not confirm unseen rear, side, top, hidden or internal structures.
- Label unseen information Undefined or Inferred.
- Do not treat perspective distortion as real structural proportion.
- Do not generate missing views unless explicitly requested or approved.
- State whether additional references are required for Full Blueprint accuracy.

## AI Artifact Filtering

Check visible features for possible AI artifacts, including malformed logos, duplicated components, inconsistent symmetry, merged accessories, random buttons, unstable patterns, incorrect limb count, impossible connections, melted edges and inconsistent material transitions.

Suspected artifacts must be labelled **Diagnostic**, **Inferred Error** or **Pending Confirmation**. They must not be preserved automatically.

## Task-Specific Reference Packages

Possible Task-specific Reference Packages include:

- Identity Package
- Angle Translation Package
- Scene Adaptation Package
- Style Translation Package
- Video Continuity Package

Rules:

- Use the minimum sufficient references.
- Select one Primary source for each important role.
- Do not use unresolved conflicting references together.
- Contextual References cannot override Identity References.
- Diagnostic References are not positive generation references.
- Explicitly exclude unrelated signals.
- More reference images are not automatically better.

## Review Gate

After presenting a text Draft, stop for user review.

The user may confirm or correct findings, reject proposed locks, approve Permanent Asset Locks, approve Controlled Variations, resolve conflicts, request more evidence, request a visual Blueprint sheet, or request direct image or video generation.

Only user-approved content may move from Proposed or Observed into Confirmed Permanent Asset Locks.

## Visual Blueprint Generation

When explicitly requested:

1. Load the approved text Blueprint.
2. Use only Confirmed information and approved Permanent Asset Locks as hard identity constraints.
3. Distinguish supplied references from generated reconstructions.
4. Do not present invented missing views as confirmed design.
5. Do not reintroduce excluded background, pose, camera, lighting or style signals.
6. Validate the visual board against the text Blueprint.
7. Keep the text Blueprint authoritative.

## Direct Generation Exception

When direct generation is explicitly requested:

- Complete Asset Intake and evidence separation internally.
- Use Confirmed information as hard constraints.
- Use Observed information only within its Approved Scope.
- Do not silently promote Inferred or Proposed content to Permanent Asset Locks.
- Execute the requested output.
- Run Global Validation, then Asset Validation.

Direct generation does not bypass identity consistency control.
