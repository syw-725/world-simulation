# YCOS (Yan Creative Operating System)

Version 1.0

---

## Overview

YCOS is an AI-agnostic operating system for creative work.

Instead of optimizing prompts, YCOS standardizes creative reasoning.

Its goal is to produce consistent, believable and commercially effective creative outputs across different AI models.

The system separates reasoning from execution.

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

When the optional Asset Blueprint module is active, it preserves reusable asset identity without replacing global world simulation, physics, materials, lighting, camera, composition, commercial judgement, scene logic or validation.

---

## Version

Current Version

YCOS v1.0
