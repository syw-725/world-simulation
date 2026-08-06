# YCOS Bootstrap Initialization

## Purpose

`BOOTSTRAP.md` initializes YCOS for a new session or execution environment. It identifies the repository, required documents, loading order and authority boundaries before a task enters the existing Build and Creative Workflow.

Bootstrap governs initialization only. It does not contain or replace the full creative reasoning, execution or validation workflow.

## Repository Context

YCOS operates from the GitHub repository `syw-725/world-simulation`.

Before claiming to follow YCOS, confirm that the repository or an equivalent workspace checkout is available and that the required files can be read. If the repository or required files are unavailable:

- do not claim that YCOS was loaded;
- do not invent or reconstruct missing rules;
- identify the missing repository context clearly;
- do not execute a `Build |` task that depends on unavailable YCOS documents.

Repository access failure is an initialization condition. It is separate from an under-defined creative project, which can be assessed only after YCOS has been initialized.

## Required Loading Order

Use this canonical loading order:

1. `BOOTSTRAP.md`
2. [BUILD_PROTOCOL.md](BUILD_PROTOCOL.md)
3. [CREATIVE_WORKFLOW.md](CREATIVE_WORKFLOW.md)
4. [VALIDATION.md](VALIDATION.md)
5. Optional documents only when applicable:
   - [Visual Translation Protocol](visual-translation/VISUAL_TRANSLATION_PROTOCOL.md)
   - [Asset Blueprint overview](asset-blueprint/README.md)
   - the applicable [Asset Blueprint Protocol](asset-blueprint/ASSET_BLUEPRINT_PROTOCOL.md), [Execution](asset-blueprint/ASSET_EXECUTION.md), [Lifecycle](asset-blueprint/ASSET_LIFECYCLE.md) and [Validation](asset-blueprint/ASSET_VALIDATION.md) documents

Do not load every optional document automatically. Load only the optional material required for the task and its applicable validation.

## Authority Order

Document authority is divided by responsibility:

- `BOOTSTRAP.md` governs initialization and document loading.
- [BUILD_PROTOCOL.md](BUILD_PROTOCOL.md) governs `Build |` activation and response behaviour.
- [CREATIVE_WORKFLOW.md](CREATIVE_WORKFLOW.md) governs creative reasoning and Execution Readiness.
- [VALIDATION.md](VALIDATION.md) governs mandatory Global Validation.
- [Visual Translation](visual-translation/VISUAL_TRANSLATION_PROTOCOL.md) is optional and governs communication-to-visual translation only.
- [Asset Blueprint](asset-blueprint/README.md) is optional and governs reusable asset identity and continuity only.

Bootstrap does not overrule or replace any of these authorities.

## Session Initialization Procedure

Initialize the session by:

1. Confirming repository or workspace availability.
2. Reading the required core documents.
3. Identifying the task type.
4. Determining whether optional Visual Translation is applicable.
5. Performing the Asset Consistency Decision at the position defined by the Creative Workflow.
6. Applying the Creative Workflow's Execution Readiness decision before visual execution.
7. Continuing through the existing Creative Workflow.
8. Running mandatory Global Validation and any applicable Asset Validation.
9. Reporting honestly if required documents or context were unavailable.

This sequence initializes and routes the task. The linked authoritative documents define the actual reasoning, execution and validation rules.

## Build Request Behaviour

For a request beginning with `Build |`:

- activate the existing Build Protocol;
- complete required reasoning internally when direct generation is requested;
- execute only when repository initialization succeeded and Execution Readiness passes;
- request targeted clarification when foundational project information is missing;
- stop after the requested analysis and execution plan when the user asks for analysis first or says not to generate.

Use [BUILD_PROTOCOL.md](BUILD_PROTOCOL.md) and [CREATIVE_WORKFLOW.md](CREATIVE_WORKFLOW.md) for the complete rules.

## Repository-Unavailable Behaviour

### Initialization Status: Repository Context Required

Use this status when the repository is not open, required documents cannot be found or the environment cannot access the repository. Identify the missing context and stop initialization.

Do not classify repository unavailability as **Ready for Execution**, **Clarification Required** or **Analysis / Direction Only**. Those outcomes apply only after YCOS initialization succeeds and the Creative Workflow evaluates the project.

Example input:

`Build | Image Gen — Japanese feeling, premium but not luxurious, ratio 4:5.`

- **Repository unavailable:** stop and report that the YCOS documents could not be loaded.
- **Repository available, project under-defined:** apply the Creative Workflow and return **Clarification Required** because the Hero Subject, deliverable, required content and commercial objective are missing.
- **Repository available, project sufficiently defined:** proceed through the existing workflow.

This example demonstrates status separation. It does not prescribe a visual style.

## Optional Module Loading

Load Visual Translation only when abstract communication intent requires translation into observable visual decisions.

Load Asset Blueprint only when reusable asset identity, consistency or continuity is relevant. Select its applicable documents and validation according to the authoritative Asset Consistency Decision; do not load the entire module when it adds no decision value.

## Initialization Completion Check

Before claiming initialization is complete, confirm:

- the repository is available;
- required core files were found and read;
- optional modules were identified only where applicable;
- no document authority was replaced;
- the task can now enter the existing Build and Creative Workflow.
