# YCOS Video Production Workflow V1

## Purpose

Video Production is a temporal extension of the existing YCOS Creative Pipeline, not a separate Video OS. The root Creative Workflow remains authoritative for Project Understanding, Creative Intent, World Simulation, physics, materials, camera, composition, Scene Locks, Variable Assets and commercial judgement. Asset Blueprint and Reference Separation remain authoritative for reusable identity and reference scope. Root Validation remains mandatory.

> YCOS owns the intelligence. External generation models receive the task they need to perform, not the YCOS brain.

## Build Trigger and Lifecycle

`Build | Storyboard > Video` starts this workflow. It does not immediately generate video.

```text
Brief → Creative Decision → Project Definition → World / Asset / Reference Resolution
→ Story → Story Approval → Storyboard → Storyboard Approval Gate
→ Shot Blueprint → Continuity Definition → Shot Validation
→ Canonical Generation Package Compilation → External Provider Boundary
→ Provider Execution → Shot Review → Revision / Regeneration → Shot Approval
→ Assembly → Final QA → Learnings
```

All existing Bootstrap, Build Protocol, Execution Readiness and validation rules remain active.

## Architectural Invariants

```text
Story ≠ Storyboard
Storyboard ≠ Video Prompt
Storyboard ≠ Shot Blueprint
Shot Blueprint ≠ Generation Package
Creative Truth ≠ Provider Execution
YCOS Knowledge ≠ External Model Context
Internal Learnings ≠ Provider Prompt
Generation Package ≠ Permanent Creative Truth
```

Creative Truth consists of approved Project Definition, Creative Decision, Story, Storyboard, World, Assets, Shot Blueprints, Continuity and Decisions. Provider Execution consists of the derived Generation Package, adapter mapping, provider/model parameters and external call. A provider change must never require rewriting a Shot Blueprint.

## Reuse and Extension Map

| Concept | Decision | Reason |
| --- | --- | --- |
| Project Definition | Extend | Optional `video` delivery fields apply only to video Projects. |
| Creative Decision | Reuse | Remains provider-neutral canonical direction. |
| World Simulation, physics and materials | Reuse | Temporal changes use the same believable-world authority. |
| Asset Blueprint and Reference Separation | Reuse | Identity, continuity risk and reference scope already exist. |
| Scene Locks and Variable Assets | Reuse | Shots select existing locks and permitted variables. |
| Visual Translation | Reuse | Motion character may inform direction without becoming execution. |
| Validation and Learnings | Extend | Add temporal checks and observations within existing systems. |
| Story, Storyboard, Shot Blueprint, Continuity | New | These are genuinely temporal production artifacts. |
| Video Generation Package and Review | New derived artifacts | They compile and assess execution without becoming creative truth. |
| Provider Boundary | Extend | Existing allowlist boundary gains shot-scoped video contracts. |

## Information Scopes and Least Context Principle

Information narrows monotonically:

1. **Scope A — YCOS Brain:** Core specifications, reusable learnings, all projects/assets and internal validation. Never exported wholesale.
2. **Scope B — Project Context:** only the current Project's approved Definition, Direction, World, Assets, Story, References and Decisions.
3. **Scope C — Shot Context:** one Story beat, Storyboard unit, Shot Blueprint, required assets/references, incoming/outgoing state, locks and permitted variations. Unrelated shots are excluded unless explicit continuity dependencies.
4. **Scope D — Generation Context:** only selected frames/references, minimum identity data, camera/motion instruction, duration, output requirements, locks and execution parameters needed for one attempt.

**Least Context Principle:** an external generation system receives the minimum sufficient, explicitly selected context for its task. Availability is not permission to export. Compilation transforms internal knowledge into production decisions and generation instructions; it never copies internal reasoning or learning histories into prompts.

## Project Definition Extension

Existing fields remain valid. A video Project may add an optional `video` object with `target_duration`, `aspect_ratio`, `platform`, `fps` and `delivery_format`. These fields are never required for non-video Projects.

## Story Specification

Story defines what happens, why it happens, narrative order and communication purpose. It does not define detailed camera execution. It records `story_id`, `project_id`, approval status, objective, message and ordered beats. Each beat has an identifier, purpose, description, target duration, required assets and transition intent.

## Storyboard Specification and Gate

Storyboard translates approved Story beats into visual sequence intent. A unit records `shot_id`, `story_beat_ref`, order, duration, frame description/composition/framing, action preview, transitions and an optional approved frame reference. A storyboard image is visual intent, not a video prompt or executable package.

Each unit uses `draft`, `revision_required` or `approved`. Partial approval is supported. Only an approved unit may proceed through the Shot Blueprint Generation Gate.

## Shot Blueprint Specification

A Shot Blueprint is the provider-neutral creative source describing what a temporal event must be. It records identity/source references, purpose/duration, World and required Assets, start/end state, camera, subject/environment motion, lighting, physics, Scene Locks, Variable Assets, allowed variation, forbidden changes and transitions. Start/end state captures meaningful subject, props, environment, material and camera state—not microscopic simulation. Provider-specific controls never belong here.

## Continuity Specification

Shots are observations of the same simulated world, not independently regenerated worlds. A Continuity record declares `state_inheritance.previous_shot`, `hard_continuity`, `soft_continuity`, explicit incoming/outgoing states and dependent shots.

Hard continuity may lock identity, face, hair, wardrobe, product/packaging/logo geometry, room geometry, object location, screen/light direction, time, exposure, material/wetness/damage/cooking/liquid/prop state and motion direction. Unresolved hard continuity blocks compilation. Soft continuity permits stated natural variation.

World Simulation and root Validation govern gravity, inertia, pressure, contact, collision, deformation, fluids, heat, steam, condensation, reflections, shadows, cloth, hair and airflow. Material changes require a physical or narrative cause.

When an approved shot is superseded, only dependent shots are flagged `continuity_review_required`; unrelated approved shots remain valid.

## Canonical Video Generation Package

The package is a reproducible compiled artifact, not creative truth:

```text
Creative Truth → Compile → Canonical Generation Package
→ Provider Adapter → Provider Request → Execution → Result
```

It identifies Project, shot and source references; strategy; explicitly selected frame/reference inputs; distilled visual, camera, motion, physics and lock instructions; output duration/aspect/resolution; capability requirements and optional provider preferences; and generation status. Strategies include `text_to_video`, `image_to_video`, `first_frame_to_video`, `first_last_frame`, `reference_to_video`, `character_reference`, `motion_reference` and `video_to_video`.

Provider/model preferences are execution metadata only. The package may be stored for audit but is regenerated when provider, model, strategy or execution controls change.

## Generation Gates

Compilation fails closed with `generation_status: blocked` unless Project Definition and approved Creative Decision exist; the Story and beat resolve; relevant World, Assets and approved References resolve; the Storyboard unit is approved; the Shot Blueprint validates; Scene Locks resolve; hard continuity and required state transitions resolve; and strategy-required frames/references exist. Missing creative decisions are never invented.

## External Provider Boundary

Only the canonical package and explicit upload manifest may cross the boundary. Allowed data is limited to selected approved frames/references, minimum identity/product references, shot instructions, necessary camera/motion/physical state, duration/aspect/output parameters and provider execution controls.

Forbidden by default: repositories, Core/system documents or schemas, Git history, other Projects, unrelated shots/assets/references, `internal/`, rationale or reasoning logs, private Decision history, global Learnings, credentials and system instructions. Context-export validation checks required inclusion and forbidden/unrelated exclusion before staging.

An adapter may map fields, format references, select supported controls, validate capabilities and report unsupported requirements. It must not redesign Story or a shot, weaken locks, change identity, or silently degrade creative intent. Unsupported critical requirements block execution or require an explicitly revised strategy. V1 has no autonomous router.

## Video Review and Approved Shot Lock

Review extends existing Validation with identity, world continuity, composition, camera/subject/environment motion, lighting, materials, physics, temporal coherence, transition quality, commercial clarity and AI artifacts. Artifacts include facial/identity drift, hand/body mutation, logo/packaging deformation, texture crawl, flicker, warping, geometry instability, duplication/disappearance, reflection/shadow inconsistency, intersections, material flicker, camera discontinuity, fake slow motion, fluid-volume errors and spatial/transition breaks.

Review records `status: pass | warning | fail`, `decision: approve | revise | regenerate | reject`, issues and recommended actions. Outputs follow `candidate → selected → approved`, with `rejected` and `superseded` available. Approved outputs are immutable references unless manually superseded.

Shot-level regeneration is the default correction unit. Downstream inherited state triggers continuity review, not automatic whole-project regeneration.

## Assembly and Learnings

V1 assembly is metadata only: ordered approved shot generations, in/out points, transition, audio and subtitle references. It is not an NLE.

Video observations remain in the existing project-local Learnings system. Global Learnings remain internal. Compilation may translate a learning into a concrete decision such as slower camera movement and strict logo locks; the learning text itself never crosses the provider boundary.

## Deferred Scope

Provider authentication/API integration, complete provider adapters, autonomous routing, automated generation loops, media generation and full editing/assembly are outside V1.
