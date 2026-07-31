# ==========================================================
# BUILD TRIGGER
# Version 1.0
# ==========================================================

## Purpose

The Build Trigger defines how every Build request is interpreted before any creative work begins.

Its purpose is to ensure that every Build task follows a consistent decision process rather than executing immediately.

Creative execution should always begin with understanding the request.



---

## Trigger

This trigger is activated whenever a request begins with:

Build |

The trigger determines the nature of the task before selecting an execution path.

Execution should never begin immediately after the trigger.



---

## Task Interpretation

The first responsibility is to identify the user's actual objective.

The workflow should interpret the intent behind the request instead of relying solely on keywords.

Typical Build tasks include:

- Image Generation
- Image Analysis
- Image Retouching
- Image Editing
- Style Transformation
- Creative Direction
- Visual Evaluation
- Commercial Design
- Product Visualization
- Food Photography
- Key Visual Development

If multiple objectives exist, they should be identified before execution.



---

## Workflow Routing

After the task has been interpreted, determine the appropriate execution path.

### Creative Tasks

Tasks requiring creative judgement must activate:

CREATIVE_WORKFLOW.md

Examples include:

- Generate
- Analyze
- Retouch
- Redesign
- Improve
- Extend
- Visual Development
- Commercial Evaluation

Creative reasoning must always be completed before execution.



### Technical Tasks

Tasks requiring only technical execution do not require the Creative Workflow.

Examples include:

- Crop
- Resize
- File Conversion
- Background Removal
- Canvas Extension
- Export
- Format Conversion

Technical tasks should execute directly without unnecessary creative reasoning.



---

## Multi-Stage Tasks

Some Build requests contain multiple creative objectives.

These should be completed sequentially rather than simultaneously.

Typical sequence:

Interpret Request

↓

Creative Reasoning

↓

Diagnosis

↓

Decision

↓

Execution

↓

Quality Evaluation

Each stage should be completed before progressing to the next.

Execution should never skip the diagnosis or decision stages.



---

## Image Analysis

Image Analysis is a reasoning task.

Its purpose is to understand an image, not to create an analysis board.

Typical analysis includes:

- Project Objective
- Composition
- Perspective
- Lighting
- Material Behaviour
- Physical Logic
- Visual Hierarchy
- AI Artifact Detection
- Commercial Evaluation

Analysis should produce creative understanding.

Visual presentation of the analysis is optional and should only be created when explicitly requested.



---

## Image Retouch

Image Retouch is a refinement task.

Retouching should always be based on the conclusions established during Image Analysis.

Retouching should improve the existing visual world rather than unintentionally creating a different one.

Unless explicitly requested, retouching should preserve:

- Scene Locks
- Creative Direction
- Composition
- Perspective
- Lighting Logic
- Material Behaviour



---

## Execution Principles

Execution should only begin after:

- The request has been interpreted.
- The correct workflow has been selected.
- A clear execution strategy has been established.

Whenever Creative Workflow is activated, reasoning always precedes execution.



---

## Guiding Principle

Build is not an execution command.

Build is the entry point into a structured creative reasoning process.

The objective is not to generate faster.

The objective is to make better creative decisions before execution.
