# YCOS Creative Pipeline Architecture

## Purpose

This document defines the orchestration boundary around the established YCOS Creative Workflow. It does not replace, restate or reinterpret creative reasoning.

The architecture is:

**One YCOS Core → many Projects → many Runs → many Providers**

## Authoritative Layers

### YCOS Core

This repository is the stable creative knowledge base. [BOOTSTRAP.md](BOOTSTRAP.md), [BUILD_PROTOCOL.md](BUILD_PROTOCOL.md), [CREATIVE_WORKFLOW.md](CREATIVE_WORKFLOW.md), [VALIDATION.md](VALIDATION.md), Visual Translation and Asset Blueprint retain their existing authority. Project tooling consumes these documents by versioned reference and must not write to them.

### Creative Workflow

The Creative Workflow remains authoritative for Project Understanding, Creative Intent, World Definition, physical logic, material and object behaviour, lighting, camera, composition, Reference Separation, Asset Blueprint, Scene Locks, Variable Assets, commercial evaluation and visual validation.

Architecture records and routes the resulting decisions. It does not create a second creative workflow.

### Project Sandbox

Commercial project data belongs in the separate private `syw-725/ycos-projects` repository. A Project Sandbox contains its manifest, private internal material, explicitly approved references and assets, versioned Creative Decisions, immutable completed Runs, outputs and project-local learnings.

Projects may identify Core dependencies by repository, document and version or commit. They must not embed or mutate Core documents. Tooling must resolve all paths within the Project repository and reject destinations in Core.

### Creative Decision

A Creative Decision is the provider-neutral canonical creative specification. Significant values carry a value, status (`locked`, `preferred` or `open`) and internal rationale. Rationale is not exported to providers automatically.

Decisions are versioned (`decision-v001`, `decision-v002`, …), never overwritten by a Run, and follow this lifecycle:

Draft → Discussion → Approved → Locked → Used by Run → Revised → Archived

A revision creates a new version. Reviews create observations; observations become Decisions only after human approval.

### Run

A Run is exactly one execution attempt and references exactly one Decision version. A completed Run is immutable. Any changed generation request creates a new Run. Runs may compile decisions and record provider results but may never modify Decisions.

### Generation Package

The Creative Compiler turns one Decision version into a provider-neutral Generation Package. This package describes objective, subject, environment, camera, composition, lighting, materials, physics, references, Scene Locks, Variable Assets, negative constraints, output requirements and media type.

Compiled prompts are disposable provider outputs. They are not canonical knowledge.

### Provider Adapter and AI Generator

A Provider Adapter receives only a Generation Package and explicit upload manifest. Its minimal contract is `validate`, `compile`, `stage`, `execute`, `collect` and `record`. Provider-specific prompts, parameters, API/CLI formats, upload and download behaviour remain in the adapter.

The external AI generator receives only the explicit export package. It receives no repository access and may not browse Core, project `internal/`, other Projects, Git history, workflow documents or unrelated references. Replacing Higgsfield with another adapter must not change the Creative Workflow.

## Security and Execution Boundary

Exports are allowlist-only. Wildcards, recursive directory uploads and repository-root uploads are forbidden. Every staged file must be named in `upload-manifest.yaml`; staging rejects missing or unexpected files.

Temporary provider inputs live in a gitignored `.ycos-staging/<project-id>/<run-id>/` directory outside logical Project data. Credentials, tokens, browser sessions and provider authentication artifacts must never enter staging, manifests, logs or Git.

External execution fails closed unless both conditions are explicit:

- `approved_for_external_generation: true`
- `execution_mode: live`

The default mode is `dry-run`. Dry Run validates and stages the allowlist without authentication, network contact, upload or credit use.

## Isolation and Learning Gate

Core is read-only from every Project. Projects are mutually isolated. Runs cannot write to Decisions or completed Runs. Providers cannot consume unrestricted repository content.

Observations and promotion candidates remain under a Project's `learnings/` directory. The default promotion status is `project_only`. Nothing automatically modifies Core.

A Core Change Proposal is separate from a Project Run and requires:

- problem;
- evidence;
- affected existing module;
- why extension is insufficient;
- compatibility assessment;
- migration impact;
- explicit human approval.

Only a separately reviewed Core change may promote project learning.

## Compatibility Rule

The pipeline surrounds the existing workflow with project, versioning, compilation, provider-routing and execution boundaries. If an architecture change would alter Creative Workflow, Build Protocol, Reference Separation, Asset Blueprint or existing validation behaviour, stop that alteration and add an adapter around the existing authority instead.

## Architecture Invariants

1. A Project cannot change YCOS Core automatically.
2. A Run cannot change a Creative Decision.
3. An external provider cannot read GitHub or either repository.
4. A provider receives no file absent from the explicit upload manifest.
5. Providers are replaceable without changing Creative Workflow.
6. One YCOS Core supports many Projects.
7. One Project supports many Runs.
8. Prompts are compiled outputs, never canonical knowledge.
9. Creative Decisions are canonical.
10. Project learning cannot enter Core automatically.
