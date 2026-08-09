# YCOS Project Bootstrap

## Purpose

Project Bootstrap is the fail-closed operational gate an execution agent must complete before creating or updating a YCOS Project. It connects the authoritative YCOS Core in `syw-725/world-simulation` to Project workspaces in the separate private `syw-725/ycos-projects` repository.

It does not define creative methodology, Project-specific direction, provider prompts or generation parameters. It never authorises or triggers generation.

## Repository Boundary

- `syw-725/world-simulation` is YCOS Core and is read-only to Project tooling.
- `syw-725/ycos-projects` contains Project workspaces and Project tooling.
- The resolved Core checkout and Project repository must be different repositories. Project tooling must reject a Project path inside Core and any attempted write to Core.
- Projects reference Core by repository, immutable revision and declared dependency; they never copy Core governance documents.
- Project-local `references/`, `sources/` or equivalent input directories contain only Project material such as briefs, approved external references and user-supplied assets. They are never searched for YCOS governance.

Core governance includes this document, `BOOTSTRAP.md`, `BUILD_PROTOCOL.md`, `CREATIVE_WORKFLOW.md`, `VALIDATION.md`, `YCOS_ARCHITECTURE.md` and Core module source documents.

## Required Sequence

Complete these steps in order:

1. Resolve the Core repository as `syw-725/world-simulation` from an explicit readable checkout.
2. Resolve an approved immutable 40-character Core commit SHA and verify that the checkout contains that commit.
3. Read Core [Bootstrap](BOOTSTRAP.md), including its Core entrypoint rules.
4. Read the [YCOS architecture boundary](YCOS_ARCHITECTURE.md).
5. Read the [Creative Workflow](CREATIVE_WORKFLOW.md).
6. Read [Validation](VALIDATION.md).
7. Resolve and read only explicitly declared additional Core dependencies. Use the existing [Asset Blueprint](asset-blueprint/README.md), its Reference Separation section in [Asset Blueprint Protocol](asset-blueprint/ASSET_BLUEPRINT_PROTOCOL.md), and [Visual Translation](visual-translation/VISUAL_TRANSLATION_PROTOCOL.md) only when relevant.
8. Confirm that every required Core document is readable at the approved revision.
9. Confirm that the Project repository is separate from Core.
10. Confirm that the task and destination cannot modify Core.
11. Resolve the Project schema and template from `syw-725/ycos-projects`; never invent missing fields or schemas.
12. Record the bootstrap result and only then allow Project creation or update.

If repository identity, revision, required documents, declared dependencies, isolation or Project schema cannot be resolved, stop. Do not reconstruct rules from memory or from Project-local inputs.

## Core Reference

Use the Project repository's existing manifest schema. A bootstrapped Project records one Core dependency equivalent to:

```yaml
core_dependencies:
  - repository: syw-725/world-simulation
    revision: 7da0de2c71f3d82ac2d6e14cf4efc5891da23014
    architecture: YCOS_ARCHITECTURE.md
    dependencies:
      - creative-workflow
      - validation
```

The revision must be an immutable full commit SHA, not `main`, `latest` or a moving tag. Dependency identifiers are resolved through the Project Bootstrap implementation to Core-owned documents; Projects do not store copies.

## Minimum Handoff

The human or ChatGPT handoff contains only operational inputs:

```yaml
project_id: ap-001
project_name: 和牛壽喜燒
project_type: YCOS Acceptance Project
core_repository: syw-725/world-simulation
core_revision: <approved 40-character commit SHA>
core_dependencies:
  - creative-workflow
  - validation
approved_creative_decision: <approved decision version or null>
project_repository: syw-725/ycos-projects
generation_block_status: blocked
```

Core rules come from the resolved Core revision. The Creative Decision comes only from the approved conversation or handoff. If it is absent, record the bootstrap as `pending_creative_decision`; do not invent a Decision or mark the Project production-ready.

## Bootstrap Record and Generation Block

The Project manifest records the Core repository and revision, declared dependencies, Project schema version, bootstrap timestamp and status, approved Creative Decision version when supplied, and `generation_allowed: false`.

`generation_allowed` is always `false` at bootstrap. A later Production / Provider Gate may separately authorise external generation under the existing architecture. Project Bootstrap itself performs no provider action.

## Completion Outcomes

- `ready`: Core, isolation and Project schema resolved, and an approved Creative Decision version was supplied. Generation remains blocked.
- `pending_creative_decision`: operational bootstrap checks passed, but no approved Creative Decision version was supplied. Metadata scaffolding may exist, but the Project is not production-ready and generation remains blocked.
- failure: no Project is created or updated when a required operational check fails.
