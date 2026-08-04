# Asset Validation

Global [VALIDATION.md](../VALIDATION.md) must be completed first. Asset Validation extends Global Validation and never replaces or lowers it.

## Validation Gates

### 1. Identity Gate

- [ ] Identity Core matches the approved Blueprint.
- [ ] Recognition Anchors are present and correctly related.
- [ ] Permanent Asset Locks remain unchanged.
- [ ] The asset is recognizable at target output size.

### 2. Structure Gate

- [ ] Silhouette is correct for the view.
- [ ] Proportions remain approved and coherent.
- [ ] Visible and hidden components translate correctly.
- [ ] Anatomy, topology, connections and articulation are valid.

### 3. Material Gate

- [ ] Intrinsic materials remain correct.
- [ ] Roughness and reflection are material-appropriate.
- [ ] Transparency, translucency and edge behaviour are coherent.
- [ ] Material appearance responds correctly to scene conditions.

### 4. Colour and Marking Gate

- [ ] Intrinsic colour is preserved under current lighting.
- [ ] Logos and markings have correct form, placement and orientation.
- [ ] Environmental colour cast has not become permanent colour.

### 5. Scene Integration Gate

- [ ] Scene scale is credible.
- [ ] Contact and support are physically correct.
- [ ] Shadows and reflections match the world.
- [ ] Moisture, heat, pressure and deformation follow their causes.
- [ ] Crop safety and composition preserve commercial readability.

### 6. Motion Gate

- [ ] Motion and articulation follow the Blueprint.
- [ ] Weight, balance, speed and secondary motion are credible.
- [ ] Motion Complexity is appropriate for the shot and tool.

### 7. Continuity Gate

- [ ] Temporary State Changes match the intended progression.
- [ ] No temporal Identity Drift is visible.
- [ ] Shot-to-shot scale, direction, costume, props, damage and wetness are continuous.
- [ ] Start and end states match the Sequence Continuity Sheet.

### 8. AI Artifact Gate

- [ ] No malformed logos, duplicated components or merged accessories.
- [ ] No impossible connections, incorrect limb count or unstable symmetry.
- [ ] No repeated AI patterns or repeated micro-textures.
- [ ] No artifact has been treated as an approved design feature.

### 9. Commercial Readability Gate

- [ ] The asset remains immediately identifiable.
- [ ] Recognition survives the target output size and duration.
- [ ] Crop safety preserves important anchors, logos and product information.
- [ ] Continuity supports the intended message, brand or IP.

## Validation Results

- **PASS** — all applicable gates pass.
- **PASS WITH MINOR FIX** — the output is usable after a small non-structural correction.
- **RETOUCH REQUIRED** — clear local errors require controlled correction.
- **REGENERATE** — broad identity, structure, view, motion or continuity failure cannot be safely corrected locally.

## Severity

- **S0 — no issue:** No applicable deviation.
- **S1 — minor:** Does not affect identity or use.
- **S2 — clear but locally repairable:** Requires a focused correction.
- **S3 — major identity or structural failure:** Requires substantial retouch or regeneration.
- **S4 — strategy failure:** Execution design, references, Blueprint, shot plan or tool capability is incorrect. Replan rather than repeat the same generation.

Result and severity are recorded separately.

## Retouch Versus Regenerate

Choose **Retouch** when:

- The error is local and its correct target is known.
- Core identity and structure remain intact.
- Correct surrounding pixels and Scene Locks can be preserved.
- Secondary effects can be reconciled reliably.

Choose **Regenerate** when:

- Identity or structure is broadly wrong.
- Multiple anchors, proportions or components have drifted.
- Motion or perspective failure affects the complete output.
- Local correction would reconstruct most of the image or shot.

At S4, do not repeat generation unchanged. Replan the Task-specific Execution Package, Reference Package, Blueprint, shot design or tool strategy first.

## Asset Validation Report

- **Result:** PASS / PASS WITH MINOR FIX / RETOUCH REQUIRED / REGENERATE
- **Blueprint:** Asset name, Version and status
- **Critical Checks:** Gates and locks evaluated
- **Detected Issues:** Evidence-based findings
- **Severity:** S0 / S1 / S2 / S3 / S4
- **Recommended Action:** Minor fix, retouch, regenerate or replan
- **Execution Decision:** Proceed, correct, regenerate, clarify or redesign

## Feedback Loop

Only recurring, predictable, identity-relevant issues with future value should be proposed for addition to Known Failure Modes.

Do not automatically write every generation error into the permanent Blueprint. Record a **Proposed Blueprint Update**, then review its evidence, future value and effect on approved identity before approval.
