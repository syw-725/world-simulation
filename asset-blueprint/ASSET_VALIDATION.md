# Asset Validation

## Purpose and Authority

Asset validation extends the mandatory root [VALIDATION.md](../VALIDATION.md). It never replaces, weakens or bypasses root YCOS validation.

Global YCOS validation runs first. Asset validation runs afterward when Level 1 or Level 2 is active. Passing asset validation cannot compensate for a failure in world consistency, physics, materials, lighting, perspective, composition, commercial purpose or another root validation requirement.

## Validation Inputs

Validate against:

- Active or Locked Asset Blueprint
- Applicable Asset Version
- Selected Controlled Variation
- Declared Temporary State
- Task-specific Reference Package
- Project Definition
- Scene Locks
- Execution Package
- Sequence Continuity Sheet, when applicable
- Produced image, retouch, shot or sequence

## Asset Validation Checks

### Identity

- Identity Core remains recognizable.
- Recognition Anchors remain present and correctly related.
- No unrelated asset identity has been introduced.

### Silhouette

- Approved silhouette logic is preserved for the view.
- Foreshortening and occlusion explain visible changes.
- Scene adaptation has not become silent redesign.

### Proportions

- Approved proportion relationships remain coherent.
- Lens, pose and perspective effects are physically explainable.
- No local generation drift has changed canonical ratios.

### Structure

- Anatomy, construction, topology and component relationships are correct.
- Articulation follows defined physical constraints.
- Components have not merged, multiplied, disappeared or changed function.

### Materials

- Canonical material identity is preserved.
- Visible response follows the authoritative scene lighting and environment.
- Material adaptation has not changed the asset into a different construction.

### Colour and Markings

- Primary colour logic remains identifiable under scene conditions.
- Markings, logos and recognition details have correct form and placement.
- Lighting-dependent colour shifts are distinguished from identity drift.

### Angle Translation

- Features translate coherently across the selected view.
- Hidden and visible components follow View Translation Logic.
- Camera distortion does not silently change identity.

### Scene Integration

- The asset obeys world, physics, contact, support, occlusion, shadow and reflection logic.
- Permanent Asset Locks and Scene Locks are both respected within their domains.
- A conflict has not been concealed as an adaptation.

### Motion

- Motion follows the assigned Motion Complexity Level and articulation logic.
- Weight, balance, inertia and deformation are credible.
- Identity anchors survive movement and occlusion.

### Temporary-State Continuity

- Temporary State entry, progression and exit are intentional.
- Pose, expression, wetness, dirt, damage, opened components, held props and scene lighting have not modified canonical identity.
- Temporary conditions return or progress according to the project plan.

### Multi-Shot Continuity

- Asset Version and Controlled Variant remain correct across shots.
- Sequence Continuity Sheet dependencies are satisfied.
- State, markings, structure, motion and camera transitions remain coherent.

### AI Artifacts

- No identity drift, topology mutation, duplicated components or unstable markings remain.
- No view-specific hallucination has been promoted as canonical identity.
- Root AI artifact checks have already passed.

### Commercial Readability

- The asset remains immediately identifiable for its intended audience and platform.
- Continuity supports rather than obscures the product, message, brand or IP.
- Recognition anchors remain readable at the required output size and duration.

## Validation Outcomes

Every asset validation produces one outcome:

- **PASS** — all applicable requirements are satisfied.
- **PASS WITH MINOR FIX** — continuity is acceptable, but a small non-structural correction is required before final delivery.
- **RETOUCH REQUIRED** — localized errors require controlled correction while preserving approved content.
- **REGENERATE** — the output has broad identity, structure, view, motion or continuity failure that cannot be safely corrected through local retouching.

The outcome and severity are recorded separately. A REGENERATE outcome with S4 severity requires replanning before another generation attempt.

## Severity Levels

- **S0 — No issue:** No relevant deviation detected.
- **S1 — Cosmetic:** Minor visible deviation that does not threaten identity or continuity.
- **S2 — Local continuity issue:** Noticeable localized drift requiring a minor fix or focused retouch.
- **S3 — Major output failure:** Significant identity, structure, motion or continuity error requiring retouch or regeneration.
- **S4 — Structural strategy failure:** The Execution Package, references, shot design, Blueprint or tool strategy is structurally wrong. Replan the strategy rather than repeating the same generation.

## Validation Record

Record:

- Root YCOS validation completion
- Asset validation outcome
- Highest severity
- Failed categories and evidence
- Affected shots or frames
- Whether the defect is scene, identity, variation, Temporary State or strategy related
- Required minor fix, retouch, regeneration or replanning action
- Confirmation after correction

Final delivery requires root YCOS validation and all applicable asset validation to be resolved at an acceptable outcome.

