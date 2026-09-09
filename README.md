# YCOS (Yan Creative Operating System)

Version 1.0

**Start here:** Read [BOOTSTRAP.md](BOOTSTRAP.md) before using YCOS in a new session or workspace.

---

## Overview

YCOS is an AI-agnostic operating system for creative work.

Instead of optimizing prompts, YCOS standardizes creative reasoning.

Its goal is to produce consistent, believable and commercially effective creative outputs across different AI models.

The system separates reasoning from execution.

YCOS uses **Cost-Aware Adaptive Capability Routing v2** to select and reassess the lowest sufficient reasoning capability and execution path at each task phase. Frontier capability is an evidenced exception, not a default. Visual rendering remains one specialised execution route inside the existing Creative Workflow.

---

## Repository Structure

### BUILD_PROTOCOL.md

Defines how Build Mode is activated and how creative tasks enter the operating system.

Responsibilities:

- Detect Build Mode
- Activate Bootstrap
- Load Creative Workflow
- Define execution flow

---

### CREATIVE_WORKFLOW.md

Defines the creative reasoning process.

Responsibilities:

- Project Definition
- World Simulation
- Physics
- Materials
- Behaviour
- Lighting
- Composition
- Scene Locks
- Variable Assets
- Creative Decision

---

### VALIDATION.md

Defines the quality control process before final output.

Responsibilities:

- Physical Consistency
- Material Realism
- Perspective Check
- Lighting Check
- AI Pattern Detection
- Commercial Quality
- Scene Consistency

---

### asset-blueprint/

Optional module for maintaining reusable asset identity and continuity across images, camera angles, scenes, styles and video shots.

- `README.md`
- `ASSET_BLUEPRINT_PROTOCOL.md`
- `ASSET_BLUEPRINT_TEMPLATE.md`
- `ASSET_EXECUTION.md`
- `ASSET_VALIDATION.md`
- `ASSET_LIFECYCLE.md`

See the [Asset Blueprint module](asset-blueprint/README.md). The core documents above remain authoritative.

### YCOS_ARCHITECTURE.md

Defines the provider-neutral orchestration boundary around the stable Core: separate Project Sandboxes, versioned Creative Decisions, immutable Runs, explicit export packages, Cost-Aware Adaptive Capability Routing v2, capability-based renderer routing, Provider Adapters and the human-approved Learning Gate. It also defines the additive, backward-compatible routing manifest contract, Astra Gate, context budgets, delta revisions and acceptance trace. It does not replace or redefine Creative Workflow.

---

## Optional Workflow Modules

[Asset Blueprint](asset-blueprint/README.md) is an optional consistency-control layer for persistent visual assets. It defines approved asset identity while Creative Workflow remains authoritative for the believable world, scene logic and commercial communication. Level 0 leaves the original workflow unchanged.

---

## Workflow

Build Request

↓

BUILD_PROTOCOL.md

↓

CREATIVE_WORKFLOW.md

↓

Cost-Aware routing assessment and phase reassessment

↓

Optional Asset Blueprint when required

Level 0 — No Blueprint continues unchanged

Level 1 — Lightweight Blueprint

Level 2 — Full Blueprint

↓

VALIDATION.md

↓

Final Output

---

## Design Principles

YCOS follows four fundamental principles:

1. Reason before execution.

2. Build the world before building the image.

3. Separate stable scene elements from variable assets.

4. Produce commercially useful creative outputs instead of visually impressive but inconsistent images.

Across those principles, use the lowest sufficient capability, keep reasoning separate from specialised execution, reassess at phase boundaries, and revise only the affected delta after Production Lock. Provider and model names remain execution records rather than Core dependencies.

When the optional Asset Blueprint module is active, it preserves reusable asset identity without replacing global world simulation, physics, materials, lighting, camera, composition, commercial judgement, scene logic or validation.

---

## Version

Current Version

YCOS v1.0

Routing Policy: YCOS Cost-Aware Adaptive Capability Routing v2
