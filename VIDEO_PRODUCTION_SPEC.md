# AI-Assisted Video Production Specification

Version: 1.3

Status: Project standard

Applies to: All video planning, storyboarding, AI generation, review, revision,
post-production, and delivery work in this project

## 1. Mandatory use

Read this document in full before beginning any video task. Use it as the
default production workflow unless the user explicitly approves a documented
exception.

This specification exists to:

- lock creative direction before expensive generation;
- maintain character, brand, and factual consistency;
- keep exact text and motion graphics under deterministic control;
- avoid unnecessary credit use and duplicated generations;
- preserve a clear approval and version history; and
- make final review repeatable rather than subjective.

No paid or credit-consuming generation may start until the applicable gates in
this document have passed and the user has approved the estimated cost.

### 1.1 Workflow standard, not a creative template

This document standardises **how a video project is run**. It does not
standardise what a video should look or sound like.

Do not inherit any of the following from an earlier project unless the user
explicitly requests it:

- visual style, medium, realism, or illustration treatment;
- characters, casting, wardrobe, hair, or performance;
- environments, locations, sets, lighting, weather, or time of day;
- products, props, food, vehicles, or other objects;
- palette, typography, iconography, framing, lenses, or camera language;
- music, VO style, sound design, pace, or transitions; or
- generation platform, model, resolution, duration, or cost level.

Every new video requires a project-specific creative pack. The permanent
workflow controls when and how that pack is created, approved, used, reviewed,
and archived.

## 2. Core production principles

1. **Approve the system before producing the set.** Create and approve one
   representative style frame before making a full storyboard or shot batch.
2. **Character assets come first.** Do not invent a placeholder likeness for a
   recurring real person when an approved character sheet is required.
3. **Separate review art from production plates.** Review boards may contain
   final text and annotations; AI-video start frames should normally use clean
   plates with exact typography and motion graphics added in post-production.
4. **Generate shots, not an entire film.** Keep scenes modular so a failed shot
   can be replaced without rebuilding the whole video.
5. **Test the riskiest shots first.** Test at least one human-performance shot
   and one information/product shot before submitting a batch.
6. **Preflight cost before submission.** Record model, settings, duration,
   number of outputs, estimated credits, and account balance.
7. **Do not trust generative text.** Legal copy, nutrition values, names,
   subtitles, logos, and brand claims must be added or verified outside the
   generative video layer.
8. **Review against a checklist.** Approval requires factual, visual,
   technical, audio, and brand checks—not only an overall impression.
9. **Record project decisions locally.** Character, environment, object, style,
   motion, and sound decisions belong in the current project's creative pack,
   not in this permanent workflow specification.
10. **Storyboard approval is a hard stop.** The user must double-check and
    explicitly approve the complete storyboard before video generation begins.
11. **Transition design precedes style-approved editing.** Review the approved
    footage, propose footage-specific transition systems, and obtain user
    confirmation before treating an edit render as the first style-approved cut.
12. **Preserve deterministic edit history.** Keep source clips immutable, keep
    every shot independently editable, and create a new version for every edit
    revision.
13. **Route capability by phase.** Apply [YCOS Cost-Aware Adaptive Capability
    Routing v2](YCOS_ARCHITECTURE.md#cost-aware-adaptive-capability-routing-v2)
    across planning, decision, production and QA. Use the lowest sufficient
    capability, prefer the appropriate specialist executor, and default to
    downgrade and delta-only revision after Production Lock.

## 3. Required inputs

Before visual production begins, collect or explicitly mark as unavailable:

### 3.1 Creative brief

- working title and objective;
- intended audience and platform;
- aspect ratio and delivery resolution;
- target duration and shot-level timing;
- required tone, pace, and visual style;
- script, voice-over, on-screen text, and CTA;
- mandatory products, food portions, props, locations, and actions;
- music and sound-design direction; and
- reference videos or images, with the role of each reference stated.

### 3.2 Project-specific creative pack

Create a production pack for every project. It records the creative decisions
that are intentionally allowed to change from project to project:

- `PROJECT_BRIEF.md` — objective, audience, format, timing, script, CTA, and
  approval owner;
- `STYLE_BOARD.md` — approved visual references, palette, medium, lighting,
  framing, typography, motion language, and explicit avoid list;
- `CHARACTER_BIBLE.md` — required only when recurring people or characters are
  used; otherwise record `not applicable`;
- `ENVIRONMENT_BOARD.md` — required when a location, set, world, or background
  must remain consistent; otherwise record `not applicable`;
- `PRODUCT_PROP_BOARD.md` — required when products, food, wardrobe, vehicles,
  tools, or other objects must remain recognisable or consistent;
- `AUDIO_DIRECTION.md` — VO, music, sound effects, pronunciation, pacing, and
  rights notes when audio is in scope;
- `STORYBOARD_APPROVAL.md` — shot list, latest approved board version, user
  approval date, and any approved exceptions;
- `TRANSITION_DESIGN.md` — approved transition system, alternatives, cut map,
  review comments, and approval status; and
- `GENERATION_MANIFEST.yaml`, `EDIT_MANIFEST.yaml`, and `QC_REPORT.md` —
  generation, deterministic edit, version, and review records.

Do not copy a previous project's creative pack as an approved default. It may
be used only as a structural template; all creative content must be replaced or
re-approved for the new project.

### 3.3 Character package — conditional

For each recurring real person or approved spokesperson:

- name and role;
- approved front, three-quarter, profile, full-body, and expression references;
- fixed hairstyle, wardrobe, accessories, makeup, and grooming notes;
- approved and prohibited poses or actions;
- likeness and third-party upload permission; and
- the platform reference-element, avatar, or character ID when available.

Do not create production character frames until this package is approved.

If no recurring person or character appears, mark the character package as
`not applicable`; do not create one merely to satisfy a checklist.

### 3.4 Environment board — conditional

When one or more environments must remain recognisable or consistent, record:

- environment name and narrative purpose;
- wide, medium, and detail references;
- layout, scale, geography, entrances, windows, furniture, and fixed landmarks;
- lighting direction, time of day, weather, season, and atmosphere;
- materials, textures, palette, depth, and level of realism;
- elements allowed to move or change;
- elements that must never appear; and
- the platform environment/reference-element ID when available.

Approve the environment board before generating production storyboards that
depend on that environment. If every scene intentionally uses a different or
non-recurring background, record the rule and mark a shared environment board
as `not applicable`.

### 3.5 Product and prop board — conditional

For every continuity-critical object, record:

- approved reference images from useful angles;
- dimensions, proportions, materials, colours, labels, and distinctive marks;
- required quantity and condition;
- how the character holds, wears, opens, uses, or interacts with it;
- whether branding and text will be generated, composited, or replaced in post;
- prohibited substitutions or redesigns; and
- the platform reference-element ID when available.

### 3.6 Brand and factual package — conditional

- official logos and permitted variants;
- brand colours, typefaces, layout rules, and safe areas;
- official product or packaging references;
- disclaimers, legal copy, and minimum display duration;
- approved factual claims, quantities, units, and terminology; and
- named reviewer responsible for factual or regulatory sign-off.

Health, nutrition, medical, legal, and financial statements require explicit
subject-matter or brand approval before final production.

## 4. Stage gates

Each stage must pass before moving to the next.

The complete production and editing path is:

```text
Brief/content lock → Character sheet / identity lock → Style direction
→ Storyboard → Pilot frame/shot → Higgsfield video generation
→ Shot-level QA → Transition Design Review → Remotion deterministic edit
→ Audio/captions/graphics → Cut-point QA → Delivery/versioning
```

Higgsfield is named here when it is the approved provider for the project; it
is not a permanent model default and may be replaced by another approved
provider without changing the workflow. The asset, animatic, rights, model, and
cost gates below remain mandatory before the applicable generation steps.

### Gate 1 — Brief lock

Confirm:

- audience, platform, ratio, resolution, and duration;
- final script and approximate reading time;
- every on-screen claim, number, unit, and CTA;
- whether people appear as live action, illustration, animation, or hybrid;
- the role of AI generation versus deterministic post-production; and
- the approval owner.

Deliverable: `brief-vNN.md` or an equivalent approved brief.

### Gate 2 — Asset and rights lock

Confirm:

- character sheet and identity reference when recurring characters are used;
- wardrobe and appearance rules when relevant;
- an approved environment board when scene continuity is required;
- an approved product/prop board when object continuity is required;
- location, style, audio, factual, and brand assets applicable to this project;
- permission to use the likeness and upload supplied assets to generation
  services; and
- all missing assets and the agreed fallback for each.

Deliverable: project-specific creative pack and asset inventory with each
conditional package marked `approved`, `pending`, or `not applicable`.

### Gate 3 — Style-frame lock

Generate only one representative high-risk frame first. If useful, compare up
to three genuinely distinct directions derived from the current project's
brief and references. Examples in previous projects are never defaults.

Approve:

- character realism and likeness;
- background treatment;
- colour, texture, lighting, and line style;
- information hierarchy and safe areas; and
- whether the selected visual can be animated reliably.

Deliverable: one approved style frame and a short style statement.

### Gate 4 — Character lock

When a recurring character is used:

- create or select a reusable reference element where the platform supports it;
- test a front-facing medium shot, a three-quarter shot, and a hand/prop shot;
- approve facial identity, hair, wardrobe, body proportions, and skin treatment;
- document prohibited changes; and
- reuse the same approved reference throughout production.

Deliverable: character reference ID and approved test frames.

### Gate 5 — Storyboard lock

For every shot, record:

- shot number and duration;
- composition and camera framing;
- subject action and facial expression;
- background and prop state;
- planned camera movement;
- motion-graphics events;
- exact on-screen text and VO cue; and
- transition into and out of the shot.

Prepare two versions when exact text or graphics are important:

1. **Review board:** includes final text, numbers, arrows, labels, and notes.
2. **Production plate:** removes text and graphics that will be recreated in
   post, leaving only the stable visual elements required for generation.

Check quantities visually. For example, six spoons must show exactly six
separate spoons—not an approximate cluster.

Deliverable: approved numbered storyboard and corresponding clean plates.

#### Mandatory user storyboard checkpoint

After the complete storyboard is assembled, stop and present the full sequence
to the user for a deliberate double-check. The user must review, at minimum:

- shot order, framing, actions, environments, products, and props;
- character identity, wardrobe, expressions, and continuity;
- quantities, labels, facts, on-screen text, VO cues, and CTA;
- individual shot durations, transitions, and total running time; and
- which elements will be generated versus added in post-production.

Record the approved storyboard version, date, reviewer, requested changes, and
explicit approval in `STORYBOARD_APPROVAL.md`.

**Hard stop:** do not create pilot videos, estimate a final batch as approved,
or submit any video-generation job until this checkpoint passes. A request to
create or revise storyboard images is not approval to generate video.

### Gate 6 — Animatic lock

Before paid video generation:

- assemble static boards at intended timings;
- add temporary VO and rough music where relevant;
- verify that viewers have enough time to read every fact and quantity;
- confirm overall duration and final logo/disclaimer hold; and
- approve pacing and shot order.

Deliverable: low-cost animatic with approved timings.

The animatic may refine timing, but it may not silently change an approved
character, environment, object, style, claim, or shot. Material changes return
the project to Gate 5 for a new user storyboard approval.

### Gate 7 — Model and cost preflight

Complete or update the Cost-Aware Routing v2 assessment before comparing
candidate models. Record all five routing signals, the Context Budget, selected
provider-neutral capability and executor classes, sufficiency rationale and
reassessment trigger. A frontier-class candidate must pass the Astra Gate with
a complete Frontier Justification; context volume or final-delivery status alone
is not sufficient evidence.

For each candidate model, record:

- model and provider;
- reason for selection;
- supported input roles and aspect ratio;
- resolution, mode, duration, output count, and audio setting;
- estimated cost per shot and total cost;
- available balance before submission; and
- expected fallback if generation fails.

Do not start a batch until the user approves the total estimated spend.

Deliverable: cost table and approved generation settings.

### Gate 8 — Pilot generation

Generate the two highest-risk shots first:

- one human-performance or identity-sensitive shot; and
- one information-dense, food, product, or object-animation shot.

Review them using Section 8. If either fails, revise the inputs, clean plates,
or motion design before generating the remaining set.

Deliverable: approved pilot clips.

### Gate 9 — Higgsfield or approved-provider batch generation

- submit one job per shot unless a model-specific reason requires otherwise;
- use small, controlled subject movements;
- avoid unnecessary walking, turning, object transfer, or lip sync;
- keep the camera move simple and singular;
- record the exact prompt, model settings, media IDs, job ID, cost, and result;
- never resubmit a pending job merely because it is taking longer than expected;
  and
- regenerate only rejected shots.

Deliverable: individually numbered generation clips and generation manifest.

### Gate 10 — Shot-level QA

Review every available generated clip independently using the applicable checks
in Section 8. Assign one of the Section 9 outcomes, record accepted trims and
known post-production fixes, and confirm that each required storyboard shot has
a usable approved or approved-with-post-fix clip.

Only the resulting usable clip set may enter Transition Design Review. A
missing, rejected, or continuity-blocked shot must be regenerated, explicitly
removed, or replaced through an approved storyboard change before editing.

Deliverable: approved shot set with shot-level QA records.

### Gate 11 — Transition Design Review

This review is mandatory after all usable video clips complete shot-level QA
and before the first style-approved edit render. Codex or the editor must first
analyse:

- the video's visual medium, such as live action, sketch, paper craft, 3D, or a
  project-specific hybrid;
- brand colours, line work, patterns, icons, products, and scene elements;
- each shot's direction, speed, zoom, gesture, and object movement;
- the visual relationship between every pair of adjacent shots;
- the narrative function of each cut: continuation, comparison, reveal, topic
  change, or CTA;
- subtitle placement and information density; and
- VO phrasing, music beats, and opportunities for transition sound effects.

Before formal editing begins, propose two or three transition systems derived
from the current project's footage and approved creative pack. Clearly mark one
as the **recommended option**. For every option, explain:

- the stylistic rationale;
- where it is and is not suitable;
- transition duration and direction;
- whether outgoing and incoming pictures overlap; and
- which approved brand or picture elements it may use.

Provide a shot-by-shot Transition Map using at least this structure:

| Cut | Visual relationship | Recommended transition | Duration | Direction / branded element | Rationale |
| --- | --- | --- | --- | --- | --- |
| 01 → 02 | Describe the adjacent shots | Name the selected treatment | Frames or seconds | Direction, overlap, or approved element | Explain the narrative and visual fit |

Generic crossfades, slides, wipes, or zooms are not formal defaults. If they are
used only to test timing, the output must be labelled **generic assembly
draft**. A generic assembly draft is not the first style-approved edit.
Transitions must respond to the project's style and content and may use
approved picture or brand elements when useful. A clean cut remains valid when
the analysis identifies it as the strongest deliberate choice.

The user may approve the complete transition system once or comment on
individual cuts in natural language. Record the system version, selected
option, per-cut exceptions, comments, reviewer, date, and approval status in
`TRANSITION_DESIGN.md`. Until the user confirms the system or affected cuts, do
not present generic transition assembly as a style-approved first edit.

Deliverable: approved transition system and complete Transition Map.

### Gate 12 — Remotion deterministic edit

Build the approved transition system as a deterministic Remotion edit:

- keep every clip independent, addressable, and editable on the timeline;
- preserve original source clips unchanged and never overwrite them;
- set each trim, visible duration, direction, and transition timing precisely;
- implement only approved overlaps and visual or branded transition elements;
- recalculate the total running time after every transition overlap or trim;
- keep the approved Transition Map traceable to the edit configuration; and
- render every modification as a new version without overwriting an earlier
  render or edit state.

The first style-approved edit render may be created only from an approved
Transition Design Review. It remains a review artifact, not a final master.

Deliverable: versioned Remotion edit and edit manifest.

### Gate 13 — Audio, captions, and graphics

Use deterministic editing or motion-graphics tools for:

- final typography and subtitles;
- exact numbers, labels, units, legal copy, and disclaimers;
- logos and brand end cards;
- ticks, arrows, boxes, crosses, icon reveals, and approved transition elements;
- VO, music, transition sound effects, and final audio mixing;
- timing trims, final colour matching, and platform-specific safe areas.

Do not ask a generative video model to reproduce a brand logo or exact long-form
text when it can be composited reliably in post. Recheck transition timing when
caption density, VO timing, graphics, or music edits alter a cut.

Deliverable: versioned review master with final audio, captions, and graphics.

### Gate 14 — Cut-point QA

Inspect every transition immediately before, during, and after the cut. Apply
the checks in Section 8.7, record failures and fixes, and repeat the inspection
after any timing, direction, overlap, caption, graphics, or audio change.

Deliverable: completed cut-point QA record for the current review master.

### Gate 15 — Final QC, approval, delivery, and versioning

Run every item in Section 8. Record the reviewer, date, version, failures,
fixes, and final approval. Confirm that the delivered master and platform
variants resolve to the approved storyboard, Transition Map, source clips,
Remotion edit version, generation manifest, edit manifest, and QC report.

Never overwrite an approved master or earlier review render. Every delivery
revision receives a new version and remains traceable to its source state.

Deliverable: approved master and versioned delivery package.

## 5. Prompt construction standard

Each shot prompt should specify:

1. output ratio and intended visual form;
2. start-frame and reference-media roles;
3. character identity and invariants when a character is present;
4. one primary subject action;
5. one primary camera move;
6. environment-board and style-board invariants applicable to the shot;
7. objects and quantities that must remain unchanged;
8. text or graphics that must remain static, when unavoidable; and
9. explicit avoid instructions for face drift, hand deformation, object
   duplication, text morphing, unwanted lip sync, new logos, and camera shake.

Prefer subtle actions such as blinking, breathing, eye shifts, small hand
adjustments, gentle push-ins, and a single graphic pulse.

## 6. File and version specification

### 6.1 Recommended structure

```text
video-project/
  project-spec/
    PROJECT_BRIEF.md
    STYLE_BOARD.md
    CHARACTER_BIBLE.md
    ENVIRONMENT_BOARD.md
    PRODUCT_PROP_BOARD.md
    AUDIO_DIRECTION.md
    STORYBOARD_APPROVAL.md
    TRANSITION_DESIGN.md
  brief/
  references/
    characters/
    brand/
    products/
    locations/
  storyboard/
    review-boards/
    production-plates/
    approved/
  animatic/
  generations/
    source/
    clips/
    rejected/
  post-production/
    source-clips/
    remotion/
    renders/
  qc/
  delivery/
  manifests/
```

### 6.2 Naming

Use stable, sortable names:

```text
project_shot-01_review-board_v01.png
project_shot-01_clean-plate_v02.png
project_shot-01_seedance-v2_v03.mp4
project_transition-map_v02.md
project_edit-manifest_v04.yaml
project_master_9x16_1080x1920_v05.mp4
```

Never overwrite an approved file. Increment the version and record why it was
replaced.

### 6.3 Generation manifest

For every generated shot, record:

```yaml
shot: 01
status: approved | revise | rejected
source_frame: path-or-media-id
character_reference: name-or-element-id
model: model-id
settings:
  aspect_ratio: 9:16
  resolution: 720p
  duration_seconds: 4
  audio: false
prompt_file: path
job_id: platform-job-id
estimated_credits: 18
actual_credits: 18
output_file: path
review_notes: ""
routing: null # optional additive YCOS Cost-Aware Routing v2 object
```

Legacy generation manifests without `routing` remain valid. When `routing`
declares `policy: ycos-cost-aware-routing-v2`, it must follow the additive
manifest contract and conditional validation rules in
[YCOS_ARCHITECTURE.md](YCOS_ARCHITECTURE.md#backward-compatible-routing-manifest).

### 6.4 Edit manifest

For every deterministic edit version, record:

```yaml
edit_version: 04
storyboard_version: path-or-version
transition_design_version: path-or-version
source_clips:
  - shot: 01
    file: immutable-source-path
    trim_in_seconds: 0.0
    trim_out_seconds: 4.0
cuts:
  - cut: 01-to-02
    transition: approved-transition-name
    duration_seconds: 0.35
    direction: approved-direction
    overlap: true
calculated_total_duration_seconds: 28.65
output_file: versioned-review-render-path
review_notes: ""
```

Source paths must resolve to immutable clips. Recalculate total duration from
the visible trimmed durations and approved overlaps rather than assuming that
the sum of source durations equals the final running time.

## 7. Credit and external-service controls

Before an external upload or generation:

- confirm that the current routing assessment passed, including the Astra Gate
  when frontier capability is selected;
- identify the exact files being transmitted and the destination service;
- confirm that the user authorised that upload and has rights to the assets;
- estimate the cost before submitting paid jobs;
- state the number of jobs and expected total spend;
- avoid duplicate submissions while jobs are pending;
- preserve job IDs and result URLs; and
- download approved results into the project workspace.

Authentication, CAPTCHA, payment, subscription, and permission prompts remain
user-controlled unless narrow prior authorisation clearly covers the action.

## 8. Final video QC specification

Review the actual rendered master from beginning to end at normal speed, then
inspect critical frames closely.

### 8.1 Story and timing

- [ ] Total duration matches the approved target.
- [ ] Shot order matches the approved storyboard and animatic.
- [ ] Each fact stays on screen long enough to understand.
- [ ] Transitions feel intentional and do not obscure information.
- [ ] The final logo and disclaimer hold meets the required duration.

### 8.2 Character continuity

- [ ] Face, age, skin tone, hairstyle, and proportions remain consistent.
- [ ] Wardrobe, accessories, badge, and brand details do not change.
- [ ] Hands, fingers, teeth, eyes, and object contact are anatomically credible.
- [ ] No face drift, flicker, sudden style change, or unwanted lip sync occurs.
- [ ] Character performance matches the intended emotion and eyeline.

### 8.3 Objects, food, and quantities

- [ ] Products and packaging do not duplicate, melt, or change shape.
- [ ] Food type, portion, count, and preparation state are correct.
- [ ] Props remain spatially consistent across the shot.
- [ ] No unintended object enters or leaves the frame.

### 8.4 Text and factual accuracy

- [ ] All Traditional Chinese characters and Cantonese wording are correct.
- [ ] Names, titles, numbers, units, inequality signs, and punctuation are exact.
- [ ] Claims match the approved factual and regulatory source.
- [ ] Subtitles match the final VO and remain inside platform safe areas.
- [ ] AI-generated placeholder text is removed or covered.

### 8.5 Brand and visual system

- [ ] Official logo assets and approved colours are used.
- [ ] Typography, icon style, line style, and colour treatment are consistent.
- [ ] Hybrid live-action and illustrated layers remain visually distinct where
      required.
- [ ] No invented logo, unapproved product design, or watermark appears.

### 8.6 Motion and image quality

- [ ] Camera motion is smooth and appropriate.
- [ ] No warping, pulsing edges, texture crawl, or background instability occurs.
- [ ] Important text and graphics remain stable during movement.
- [ ] Resolution, frame rate, aspect ratio, and compression meet delivery specs.
- [ ] No unintended black frames, freezes, or corrupted media occur.

### 8.7 Cut-point QA

For every transition, inspect frames immediately before, during, and after the
cut:

- [ ] No black frame or blank frame appears.
- [ ] No unintended double exposure appears.
- [ ] No seam, white edge, or background gap appears.
- [ ] The transition does not obscure a person, product, label, or key text.
- [ ] Character scale and position do not jump unexpectedly.
- [ ] Transition timing, direction, overlap, and style match the approved Map.

### 8.8 Audio

- [ ] VO is intelligible, correctly pronounced, and appropriately paced.
- [ ] Music supports rather than competes with the VO.
- [ ] Sound effects align with visual events and are not excessive.
- [ ] Loudness is consistent and there is no clipping, noise, or abrupt cutoff.
- [ ] Required music, voice, and sound-effect rights are documented.

### 8.9 Delivery

- [ ] Master filename and version are correct.
- [ ] Required platform variants are included.
- [ ] Thumbnail, caption file, transcript, and disclaimer assets are included
      when required.
- [ ] Approved source clips, project files, manifest, and QC record are archived.
- [ ] The approved Transition Map and Remotion edit version are archived.
- [ ] Final approver and approval date are recorded.

## 9. Review outcome categories

Assign each shot one status:

- **Approved:** suitable for final post-production.
- **Approved with post fix:** generation is usable; text, colour, timing, crop, or
  graphics require deterministic editing.
- **Regenerate:** identity, anatomy, object integrity, performance, or motion
  cannot be corrected reliably in post.
- **Rejected:** contradicts the brief, factual requirements, brand rules, or
  safety and rights constraints.

Do not regenerate a shot for an issue that can be corrected faster and more
reliably in post-production.

## 10. Workflow lessons incorporated from prior production

These are workflow lessons, not creative defaults. They must not carry a prior
project's visual style, setting, cast, objects, or model choice into a new
project.

### 10.1 Watsons pilot — transition-design process learning

The Watsons pilot's first assembly used generic crossfades and slides before
footage-specific transition options were proposed. Later review established a
project-specific hybrid live-action and hand-drawn sketch language. The final
edit then used Watsons teal, irregular hand-drawn edges, and cut-specific zoom,
sketch wipe, slide, direct cut, and crossfade treatments.

Those visual choices belong only to that approved project; Watsons, teal,
sketch, hybrid treatment, and its transition mix are not defaults for future
work. The reusable process learning is that every future project must complete
Transition Design Review before a style-approved first edit is rendered.

### 10.2 General production learnings

- generating a recurring character before receiving and approving the character
  package causes avoidable identity revisions;
- generating recurring environments without an approved environment board
  causes layout, lighting, and world-continuity drift;
- generating continuity-critical products or props without an approved board
  causes shape, quantity, colour, label, and interaction errors;
- deciding the project's visual treatment after storyboarding causes avoidable
  rebuilds, regardless of which treatment is ultimately selected;
- AI-generated Traditional Chinese and Cantonese text required correction;
- exact object counts and quantities require explicit visual verification;
- final-state graphics embedded in start frames limited true reveal animation;
- sequential image generation was more reliable than simultaneous generation in
  the available workflow;
- tool/plugin discovery should precede browser automation for a named platform;
- cost estimation before submission successfully controlled the six-shot batch;
- six modular clips made selective replacement practical; and
- a full user storyboard double-check must occur before any video generation;
- visual review by the user is essential, but a recorded technical, continuity,
  brand, and factual QC pass is still required before final delivery; and
- project-specific creative decisions belong in that project's creative pack,
  while only reusable workflow lessons belong in this specification.

## 11. Project close-out record

At the end of each project, record:

- what was approved and delivered;
- total generation and post-production cost;
- rejected and regenerated shots;
- approved transition system, per-cut exceptions, and final edit version;
- transition or cut-point failures and their fixes;
- recurring failure modes;
- changes required to this specification; and
- the specification version used.

Update this document only through a reviewed version-controlled change so future
projects retain a clear history of why the workflow evolved.
