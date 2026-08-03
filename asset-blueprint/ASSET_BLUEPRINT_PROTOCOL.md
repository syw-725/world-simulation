# Asset Blueprint Protocol

## Purpose

The Asset Blueprint Protocol defines how an optional Asset Blueprint is selected, created, reviewed, activated and applied within YCOS.

It maintains reusable asset identity without replacing the authoritative world, physics, material, lighting, camera, composition, commercial and scene reasoning in the root [Creative Workflow](../CREATIVE_WORKFLOW.md).

## Asset Consistency Decision

After Project Understanding / Project Definition and before detailed execution, determine the required activation level.

### Level 0 — No Blueprint

Use when persistent asset consistency is not required. Continue through the original YCOS workflow unchanged.

### Level 1 — Lightweight Blueprint

Use for limited or medium-risk consistency. Complete sections 1–12 of the [Asset Blueprint Template](ASSET_BLUEPRINT_TEMPLATE.md).

### Level 2 — Full Blueprint

Use for persistent, multi-angle, multi-scene, video, brand, product, IP or high-risk continuity. Complete sections 1–25 of the same template.

The Full Blueprint extends the Lightweight Blueprint rather than replacing it with an incompatible format. Activation is optional and does not create another YCOS mode or Bootstrap sequence.

## Asset Intake

A Blueprint may be created from:

- Text
- One image
- Multiple images
- Text and image combined

The intake workflow is:

1. **Input classification** — identify the available source types and intended asset use.
2. **Reference Separation** — separate sources and assign each source an explicit Reference Role.
3. **Observable extraction** — record directly visible or explicitly stated information without adding assumptions.
4. **Uncertainty mapping** — identify missing, ambiguous, inconsistent or conflicting information.
5. **Draft Blueprint** — organize the evidence without treating the draft as approved identity.
6. **User review** — confirm, reject, revise or leave content unresolved.
7. **Activation** — activate the reviewed Blueprint at Level 1 or Level 2. Locking remains a separate lifecycle decision.

## Evidence Status

Every extracted or drafted statement must use one of these statuses:

- **Confirmed** — explicitly approved by the user or an approved authority.
- **Observed** — directly visible or present in a source but not confirmed as canonical.
- **Inferred** — reasoned from available evidence but not directly established.
- **Proposed** — a design suggestion awaiting approval.
- **Undefined** — not established by available sources.
- **Conflicted** — supported by incompatible sources or instructions.

Observed, Inferred or Proposed content must not automatically become a Permanent Asset Lock. Promotion to a Permanent Asset Lock requires deliberate approval and change control.

## Source Authority

Use this authority order within each source's approved scope:

1. Latest explicit user instruction
2. Locked Asset Blueprint
3. User-designated Primary Reference
4. Confirmed Active Blueprint content
5. Secondary Reference
6. Contextual Reference
7. Observed but unconfirmed content
8. Inference
9. Proposed design suggestion

Authority is scoped, not global. A Primary pose reference does not overwrite asset colour, identity, material, costume or structure unless those scopes were explicitly approved.

A latest explicit user instruction has authority for the current task, but an instruction that affects locked identity must enter the four-way change classification. It must not silently rewrite a Locked Blueprint.

### Diagnostic Reference

A Diagnostic Reference is used to identify errors, drift or undesirable outcomes. It is never used as a positive identity source.

## Reference Roles

Supported Reference Roles are:

- Identity Reference
- Structure Reference
- Proportion Reference
- Angle Reference
- Material Reference
- Colour Reference
- Pose / Interaction Reference
- Motion Reference
- Camera Reference
- Environment Reference
- Lighting Reference
- Style Reference
- Diagnostic Reference

Every reference entry must record:

- Source
- Role
- Authority
- Approved scope
- Excluded signals
- Confidence
- Notes

## Reference Packages

Create a task-specific Reference Package for each execution. Include only references needed for the task and their approved scopes. Do not load all references by default.

A Reference Package must distinguish positive identity sources from Diagnostic References and preserve excluded signals. Selection for one task does not change the authority or canonical status of the underlying Blueprint.

## Asset Locks and Scene Locks

Permanent Asset Locks and Scene Locks govern separate domains.

**Permanent Asset Locks** govern intrinsic asset identity, including approved silhouette, proportions, structure, markings, materials, primary colour logic, logos and recognition anchors.

**Scene Locks** govern the current project world, including environment, camera, lighting, composition, perspective and hero placement.

Neither category silently overwrites the other. Scene conditions may affect visible appearance but may not silently redesign identity. Asset identity may inform scene planning but may not silently override authoritative world or scene reasoning.

When a genuine conflict occurs:

1. Detect and record the conflict.
2. Determine whether the requested outcome is a scene adaptation, Controlled Variation, Temporary State Change or New Version / Redesign.
3. Preserve both approved authorities where possible.
4. Request clarification or create a deliberate asset revision when they cannot coexist.

## Four-Way Change Classification

### 1. Permanent Asset Locks

Canonical intrinsic identity approved for the current asset version.

### 2. Controlled Variations

Approved reusable states or designs within the same asset version. A Controlled Variation must define what changes, what remains locked and where the variation is permitted.

### 3. Temporary State Changes

Shot-, scene- or sequence-specific conditions that do not modify canonical identity. These may include pose, expression, wetness, dirt, damage, opened components, held props or scene lighting.

### 4. New Version / Redesign

A deliberate change to Permanent Asset Locks or core identity. Changes to core silhouette, proportions, structure, logos, primary colour logic or recognition anchors require a new major asset version.

## Conflict Handling

Do not resolve Conflicted information through silent inference.

Record:

- Conflicting sources or instructions
- Their roles, authorities and approved scopes
- The affected Blueprint fields
- Whether the conflict can be isolated as a Controlled Variation or Temporary State
- The user decision or deliberate revision required

Until resolved, preserve the last approved Active or Locked content within its scope.

## Activation Output

An activated Level 1 or Level 2 Blueprint must identify:

- Asset Version
- Lifecycle state
- Activation level
- Confirmed identity content
- Permanent Asset Locks, if any
- Controlled Variations
- Permitted Variation
- Unresolved, Undefined or Conflicted content
- Applicable references and scoped authority

Task execution then follows [Asset Execution](ASSET_EXECUTION.md), the root Creative Workflow and mandatory root Validation.

