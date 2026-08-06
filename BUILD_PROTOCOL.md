==========================================================
YCOS (Yan Creative Operating System)
Version 1.0
==========================================================

MISSION

YCOS is an AI-agnostic operating system for creative work.

It is designed to standardize how creative tasks are executed, regardless of which AI model is used.

The system separates reasoning from execution.

Every creative output should first establish a believable world before producing any final result.

==========================================================
MODES
==========================================================

YCOS contains multiple operating modes.

Build Mode
Creative image generation, image analysis, image retouching, design and visual development.

Analyze Mode
Research, critique, diagnosis and evaluation.

Research Mode
Knowledge gathering, comparison and investigation.

Strategy Mode
Planning, business thinking and creative direction.

Future modes can be added without changing existing ones.

==========================================================
BUILD MODE
==========================================================

Build Mode is activated whenever the user starts with:

Build |

Examples:

Build | Image Gen
Build | Image Analyze
Build | Image Retouch
Build | Key Visual
Build | Food Photography

Entering Build Mode does NOT immediately generate an image.

It first enters the Bootstrap process.

==========================================================
BOOTSTRAP
==========================================================

When Build Mode is detected, the AI must pause execution.

The AI asks:

Use Bootstrap?

① Yes
② No

If "No" is selected,
execute the task normally.

If "Yes" is selected,
the complete Build Workflow becomes the default reasoning process for the entire task.

==========================================================
BOOTSTRAP PROCESS
==========================================================

Bootstrap automatically performs:

1. Activate Build Mode

2. Load Creative Workflow

3. Determine task type

4. Perform the optional Asset Consistency Decision after Project Understanding

5. Execute reasoning

6. Make creative decisions

7. Execute image generation, analysis or retouching

The optional Asset Consistency Decision identifies persistent visual assets when Build Mode is active. Level 0 — No Blueprint continues normally, Level 1 — Lightweight Blueprint loads or creates a Lightweight Blueprint, and Level 2 — Full Blueprint loads or creates a Full Blueprint as defined by [Asset Blueprint](asset-blueprint/ASSET_BLUEPRINT_PROTOCOL.md). Asset Blueprint is optional, does not replace Creative Workflow, and does not create another mode or Bootstrap sequence.

This happens once only.

The workflow remains active until the task finishes.

==========================================================
BUILD WORKFLOW
==========================================================

Once Bootstrap is activated:

All image-related work must follow Creative Workflow.

This includes:

• Image Generation

• Image Analysis

• Image Retouching

• Style Transfer

• Visual Diagnosis

• Creative Direction

• Commercial Design

No image-related task may bypass the workflow.

==========================================================
BUILD HEADER
==========================================================

Whenever Bootstrap is active, every Build task begins with:

====================================

BUILD MODE

Bootstrap : ON

Workflow : Creative Workflow

Status : Reasoning Started

====================================

If this header does not appear,
the workflow has not been activated correctly.

==========================================================
END
==========================================================
