# Asset Blueprint Template

Use this human-readable template to document a reusable asset. It is not a complete generation prompt or a machine-readable schema.

For **Level 1 — Lightweight Blueprint**, complete sections 1–12.

For **Level 2 — Full Blueprint**, retain sections 1–12 and extend the same record through sections 13–25.

Every assertion derived during intake must carry an evidence status: Confirmed, Observed, Inferred, Proposed, Undefined or Conflicted. Observed, Inferred and Proposed content must not automatically become a Permanent Asset Lock.

## Lightweight Blueprint

## 1. Basic Information

- Asset name and identifier
- Asset category
- Intended use and commercial role
- Activation level
- Asset Version using MAJOR.MINOR
- Lifecycle state
- Blueprint owner or approving authority

## 2. Asset Intake Record

- Input type: text, one image, multiple images, or text and image combined
- Input classification
- Reference Separation record
- Observable extraction
- Uncertainty map
- Draft date and review status
- Activation decision

## 3. Identity Core

- Concise identity definition
- Essential identity traits
- Intended recognition across scenes, angles, styles and shots
- Evidence status and confidence for each trait

## 4. Recognition Anchors

- Primary recognition anchors
- Secondary recognition anchors
- Required relationships among anchors
- Viewing conditions under which each anchor remains important

## 5. Silhouette Logic

- Defining outer contour
- Proportion rhythm and mass distribution
- Silhouette features that must survive angle and style translation
- Permitted silhouette variation

## 6. Permanent Asset Locks

- Approved silhouette locks
- Approved proportion locks
- Approved structural locks
- Approved markings, logos and primary colour logic
- Approved material identity
- Other locked recognition anchors
- Approval source and date

## 7. Controlled Variations

For each approved reusable variation:

- Variation name
- Purpose
- Properties allowed to change
- Permanent Asset Locks preserved
- Approved use conditions
- Reference scope

## 8. Permitted Variation

- Acceptable non-canonical variation ranges
- Scene-dependent adaptation boundaries
- Temporary State boundaries
- Changes requiring clarification
- Changes requiring New Version / Redesign

## 9. Reference Roles

For each Identity, Structure, Proportion, Angle, Material, Colour, Pose / Interaction, Motion, Camera, Environment, Lighting, Style or Diagnostic Reference, record:

- Source
- Role
- Authority
- Approved scope
- Excluded signals
- Confidence
- Notes

Identify task-specific Reference Package rules. Diagnostic References must never act as positive identity sources.

## 10. Known Failure Modes

- Common identity drift
- Silhouette or proportion failures
- Structural errors
- Material, colour or marking drift
- Angle, scene, style or motion failure patterns
- Diagnostic indicators

## 11. Prompt Anchors

- Model-neutral Identity Anchor
- Model-neutral Structural Anchor
- Model-neutral Integrity Anchor
- Required identity language
- Prohibited identity-breaking interpretation

Prompt Anchors express continuity requirements. They are not a complete generation prompt or a model-specific adapter.

## 12. Basic Asset QA

- Identity recognizable
- Recognition anchors preserved
- Silhouette and proportions acceptable
- Permanent Asset Locks preserved
- Controlled Variation or Temporary State correctly classified
- Known failure modes absent or documented
- Ready for Lightweight Blueprint use

## Full Blueprint Extension

## 13. Physical Structure

- Construction, anatomy or topology
- Component relationships
- Functional parts
- Articulation and support
- Physical constraints

## 14. View Translation Logic

- Front, side, rear, three-quarter, elevated and low-angle translation
- Hidden-to-visible feature relationships
- Occlusion rules
- Foreshortening risks
- Recognition anchors by view

## 15. Material and Surface Behaviour

- Canonical material identity
- Roughness, reflection, transparency and translucency
- Thickness, edge behaviour and wear
- Environmental response boundaries
- Distinction between material identity and scene-dependent appearance

## 16. Colour System

- Primary colour logic
- Secondary and accent colours
- Markings, logos and placement
- Permitted lighting-dependent shifts
- Prohibited colour drift

## 17. Camera Translation Rules

- Lens and perspective risks
- Distance and scale behavior
- Distortion limits
- Camera conditions requiring additional references
- Identity preservation without overriding Scene Locks

## 18. Motion and Articulation Logic

- Motion capabilities and constraints
- Joint, component or deformation behavior
- Weight, balance and inertia
- Motion Complexity Levels supported
- Identity anchors that must persist during motion

## 19. Scene Adaptation Rules

- Interaction with environment and Scene Locks
- Lighting and atmospheric adaptation
- Contact, support, reflection, shadow and occlusion requirements
- Conditions that require conflict review

## 20. Style Translation Rules

- Identity features that must survive style changes
- Acceptable abstraction
- Material and colour interpretation boundaries
- Prohibited redesign disguised as style translation

## 21. Image-to-Video Continuity

- Starting-image continuity requirements
- Temporal identity preservation
- Allowed Temporary State progression
- Motion and camera continuity
- Sequence Continuity Sheet requirements

## 22. Source Authority

- Scoped authority order
- Primary, Secondary and Contextual References
- Confirmed Active Blueprint content
- Observed but unconfirmed content
- Inferences and proposed design suggestions
- Diagnostic References
- Scope limitations and excluded signals

## 23. Conflict Log

For every conflict, record:

- Date and affected fields
- Conflicting sources or instructions
- Authority and approved scope of each source
- Evidence status
- Classification decision
- Resolution, clarification required or deliberate revision

## 24. Versioning and Change Control

- Current Asset Version
- Minor revision history
- Major version history
- Permanent Asset Lock changes
- Controlled Variation approvals
- Temporary State boundaries
- Deprecated or Archived versions

Keep Asset Version, Controlled Variant, Temporary State, Project Configuration and Git commit history separate.

## 25. Full Asset Validation

- Root YCOS validation completed first
- Asset validation result
- Severity level
- Identity, structure and material findings
- Angle, scene and motion findings
- Temporary-state and multi-shot continuity findings
- Required retouch, regeneration or replanning action
- Approval for Full Blueprint use

Use [Asset Validation](ASSET_VALIDATION.md) for the complete validation procedure.
