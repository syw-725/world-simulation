# Asset Lifecycle

## Purpose

The Asset Lifecycle controls how a Blueprint moves from source intake to approved use, later replacement and archival. It prevents observations, temporary output conditions and project decisions from silently becoming canonical identity.

## Lifecycle States

### Intake

Sources have been received and are undergoing input classification, Reference Separation, observable extraction and uncertainty mapping. No Blueprint authority is implied.

### Draft

A preliminary Blueprint has been assembled. Content retains its evidence status and is not yet active for execution.

### Review

The Draft is being checked, clarified and approved. Conflicted and Undefined content remains visible. Observed, Inferred or Proposed content does not become a Permanent Asset Lock without deliberate approval.

### Active

The reviewed Blueprint may guide execution. Confirmed Active Blueprint content has source authority within its approved scope, but not all Active content is necessarily a Permanent Asset Lock.

### Locked

Permanent Asset Locks and other approved canonical content are frozen for the current Asset Version. A latest explicit user instruction may direct a change, but the change must be classified and recorded rather than silently mutating the Locked Blueprint.

### Deprecated

The Blueprint or Asset Version should not be selected for new work. It remains available for compatibility, continuity and historical interpretation.

### Archived

The Blueprint or Asset Version is retained as a historical record and is not used for active execution unless deliberately restored through review.

## Lifecycle Transitions

Normal progression is:

Intake → Draft → Review → Active → Locked → Deprecated → Archived

A Blueprint may return from Review to Draft for correction, or from Active to Review when unresolved issues emerge. A Locked Blueprint requiring an identity change or a Permanent Asset Lock change requires a new major version; it is not edited silently in place.

Deprecation and archival do not delete historical identity records.

## Asset Version

Use `MAJOR.MINOR` format, such as:

- `1.0`
- `1.1`
- `2.0`

### Minor Revision

Increment MINOR only when clarification, documentation improvement or compatible refinement does not alter core identity or Permanent Asset Locks. Minor revisions may not change core identity or Permanent Asset Locks.

### Major Version

Increment MAJOR when core identity or Permanent Asset Locks change. Changes to core silhouette, proportions, structure, logos, primary colour logic or recognition anchors require a new major version.

A major version is a New Version / Redesign and must pass intake, review, activation and validation appropriate to its risk.

## Controlled Variant

A Controlled Variant is an approved reusable state or design within one Asset Version. It does not receive a separate major identity unless it changes Permanent Asset Locks.

Record:

- Variant name
- Parent Asset Version
- Approved change scope
- Preserved Permanent Asset Locks
- Approved references
- Use conditions
- Validation status

## Temporary State

A Temporary State is limited to a shot, scene, sequence or Project Configuration. It may include pose, expression, wetness, dirt, damage, opened components, held props or scene lighting.

A Temporary State:

- Does not change the Asset Version
- Does not become a Controlled Variant automatically
- Does not modify Permanent Asset Locks
- Must define its scope, entry condition, progression and exit condition when continuity matters
- May be promoted only through deliberate review and classification

## Project Configuration

A Project Configuration records the Asset Version, Controlled Variant, Temporary State, Scene Locks and other selections used for a particular project.

It does not redefine the Blueprint and must remain separate from canonical asset identity.

## Git Commit History

Git commit history records repository document changes. It is not the Asset Version, lifecycle state, Controlled Variant, Temporary State or Project Configuration.

Asset lifecycle and version decisions must be stated inside the Blueprint rather than inferred from commit identifiers.

## Four-Way Change Control

Classify every requested asset change as:

1. Permanent Asset Locks
2. Controlled Variations
3. Temporary State Changes
4. New Version / Redesign

For each decision, record the request, affected scope, source authority, evidence status, compatibility impact, required approval and resulting Asset Version or variant/state assignment.

## Lock Promotion

Before content becomes a Permanent Asset Lock:

1. Confirm the source and approved scope.
2. Resolve or record conflicting evidence.
3. Change the evidence status to Confirmed through deliberate review.
4. Assess impact on existing variants, projects and sequences.
5. Record the lock in the current version or create a new major version when core identity changes.

Observed, Inferred or Proposed content cannot bypass this process.

## Deprecation and Archival

When deprecating or archiving a Blueprint or version, record:

- Reason
- Replacement version, if any
- Affected Controlled Variants and projects
- Compatibility or migration notes
- Date and approving authority

Existing projects may retain a Deprecated version when continuity requires it. New work should use the current approved version unless explicitly directed otherwise.
