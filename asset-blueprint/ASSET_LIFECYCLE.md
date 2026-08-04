# Asset Lifecycle

## Purpose

Asset Lifecycle defines Blueprint status, Asset Version, change control, compatibility and long-term repository storage without confusing project state or Git history with asset identity.

## Statuses

### Intake

- Unverified source material
- No Permanent Asset Locks
- No formal generation authority

### Draft

- Structured but provisional
- May include Observed, Inferred, Proposed, Undefined and Conflicted content
- Testing only

### Review

- Awaiting user decisions
- Must include a Decision Summary of confirmed content, proposed locks, conflicts and open questions

### Active

- Approved for real generation
- Revisions are allowed with records
- Confirmed content has authority within its Approved Scope

### Locked

- Core identity is formally approved
- Changes to Permanent Asset Locks require a new major Asset Version

### Deprecated

- Retained for history
- Not for new work
- Must record the replacement version when one exists

### Archived

- Cancelled or unused concepts and historical exploration
- Not active generation authority

## Blueprint Versioning

Use `MAJOR.MINOR`, such as `1.0`, `1.1` and `2.0`.

### Minor Revision

A minor revision may add or improve:

- Documentation
- New references
- Known Failure Modes
- Prompt Anchors
- Clarified material behaviour
- Additional angle information
- Validation guidance

A minor revision must not change core identity or Permanent Asset Locks.

### Major Version

A new major Asset Version is required for changes to:

- Silhouette
- Proportions
- Structure
- Logo
- Primary colour system
- Facial identity
- Required accessory
- Product form
- Core material
- Other major identity characteristics

Locked identity and Permanent Asset Locks are never changed through a minor revision.

## Distinct Records

### Asset Version

The approved identity definition identified by MAJOR.MINOR.

### Controlled Variant

An explicitly approved reusable variation within one Asset Version. It records changed and unchanged elements and does not alter Permanent Asset Locks.

### Temporary State

A scene-, shot- or sequence-specific condition such as wetness, dirt, damage, pose, held prop or temporary costume. It does not modify the Asset Version.

### Project Configuration

The Asset Version, Controlled Variant, Temporary State, Scene Locks and execution selections used by a project.

### Git Commit

A repository history record. A Git commit is not an Asset Version, Controlled Variant, Temporary State or Project Configuration.

## Change Control

Classify every proposed change as:

1. Permanent Asset Lock
2. Controlled Variation
3. Temporary State Change
4. New Version or Redesign

Project findings become **Proposed Blueprint Updates** before approval. Observed, Inferred or Proposed content cannot silently enter an Active or Locked Blueprint.

For each approved change, record:

- Source and reason
- Evidence Classification
- Approved Scope
- Changed and unchanged elements
- Approval authority
- Compatibility impact
- Resulting Version, Controlled Variant or Temporary State

## Compatibility Checks

Before activating a revision or major version, check:

- Previous references
- Previous footage
- Previous projects
- Prompt Anchors
- Angle sets
- Appearance beside the old version

Record whether each source or output remains compatible, requires migration, must remain tied to the old version or is no longer authoritative.

## GitHub Storage Principles

Long-term records may include:

- Blueprint Markdown
- Reference Index
- Source Authority
- Version History
- Change Log
- Known Failure Modes
- Validation Notes
- External reference links

Do not store by default:

- Every failed image
- All temporary keyframes
- Every prompt experiment
- Large video files
- Disposable Task-specific Execution Packages
- Unapproved random references

Git history documents changes to the specification. It does not replace Blueprint review, approval or Asset Version records.
