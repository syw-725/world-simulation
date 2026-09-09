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

The Creative Compiler turns one Decision version into a provider-neutral Generation Package. This package describes objective, subject, environment, camera, composition, lighting, materials, physics, references, Scene Locks, Variable Assets, negative constraints, output requirements and media type. When rendering capability is assessed, the package also carries the provider-neutral target capability, approved lock references, permitted variance and any required transition references.

Compiled prompts are disposable provider outputs. They are not canonical knowledge.

### Cost-Aware Adaptive Capability Routing v2

Cost-Aware Adaptive Capability Routing v2 extends the existing routing boundary; it does not create a second workflow. Creative Workflow remains the source of creative decisions. Routing selects the lowest sufficient reasoning capability and execution path for the current phase, then reassesses rather than binding the whole task to one model or executor.

Every routing assessment records these provider-neutral signals:

- `reasoning_complexity` — depth, ambiguity, dependency count and synthesis required;
- `error_cost` — consequence and reversibility of a wrong decision or execution;
- `generation_volume` — expected number and size of variants, assets or repeated operations;
- `context_weight` — amount, diversity and authority structure of required context;
- `execution_specialization` — whether a specialist executor can perform the approved operation more directly and reliably.

Signals may use project-defined scales, but a manifest must use one consistent scale and declare it. A routing outcome records the task phase, selected provider-neutral capability class, selected executor class, sufficiency rationale, cost constraint and reassessment trigger.

#### Frontier Justification and Astra Gate

Frontier-class reasoning is never selected solely because it is available, new or near final delivery. The operational **Astra Gate** applies to any frontier-class model and therefore does not make the Core dependent on an OpenAI model name.

The Gate passes only when a Frontier Justification records:

1. the specific unmet requirement or high-cost risk;
2. task-specific evidence from a lower-capability attempt, validation result or defensible pre-execution risk assessment;
3. why clarification, decomposition, retrieval, reconfiguration or a specialist executor is insufficient;
4. the expected benefit relative to added cost;
5. a bounded scope and explicit exit or downgrade condition.

Without this evidence, validation rejects frontier escalation. The Run records the actual provider and model only after the provider-neutral Gate decision.

#### Context Budget

A Context Budget is established before heavy context loading. It lists required sources, authority priority, allowed context or summarisation limit, current usage and overflow action. If the budget would be exceeded, the router preserves locked requirements and the current Decision, then uses targeted retrieval, summaries or bounded batches. It may request clarification or report blocked when authoritative conflicts cannot fit or be safely resolved. Context overflow alone is not evidence for Astra escalation.

#### Delta Revision and Production Lock

Production Lock begins when the execution strategy and its acceptance criteria are approved. After Production Lock, the default routing action is downgrade to the lowest sufficient production or QA capability. A revision identifies the failed criterion or requested change, affected fields and declared dependencies; it preserves all other Decision fields, Scene Locks and asset constraints. Full re-exploration requires evidence that the approved foundation is invalid.

#### Executor Separation

Reasoning produces a provider-neutral Decision and acceptance criteria. Execution occurs through the most suitable specialised executor or Provider Adapter. When `execution_specialization` indicates an adequate specialist, the router must prefer it before escalating general reasoning capability. Executors receive a bounded package and may not silently redefine the Decision.

### Backward-Compatible Routing Manifest

Routing v2 is an additive contract. Existing Project manifests, Decisions, Generation Packages and Runs without a `routing` object remain valid and use legacy routing behaviour. Writers may add the following object without renaming or changing existing fields:

```yaml
routing:
  policy: ycos-cost-aware-routing-v2
  signal_scale: low-medium-high
  phase: brainstorm
  signals:
    reasoning_complexity: medium
    error_cost: low
    generation_volume: high
    context_weight: low
    execution_specialization: medium
  context_budget:
    required_sources: []
    authority_priority: []
    limit: project-defined
    used: project-defined
    overflow_action: targeted-retrieval
  selected_capability: standard-reasoning
  selected_executor: general-reasoning
  sufficiency_rationale: "Sufficient for divergent concept exploration."
  cost_constraint: project-defined
  reassess_on: decision-selection
  production_lock: false
  delta_revision: null
  frontier_justification: null
  history: []
```

When active, the conditional records use these additive shapes:

```yaml
frontier_justification:
  unmet_requirement: "Cross-document conflict with irreversible production impact."
  evidence: []
  insufficient_alternatives: []
  expected_benefit_vs_cost: "project-defined"
  bounded_scope: "Resolve the named conflict only."
  exit_condition: "Return to standard reasoning after the Decision is locked."

delta_revision:
  trigger: "failed criterion or requested change"
  affected_fields: []
  dependencies: []
  preserved_locks: []
  revalidation_scope: []
```

Fields under `routing` are optional for legacy readers. V2-aware writers preserve unknown existing fields, and v2-aware validators distinguish a missing routing object (legacy-compatible) from a present but invalid v2 object. When `policy: ycos-cost-aware-routing-v2` is present, all five signals, phase, capability, executor, sufficiency rationale, cost constraint and reassessment trigger are required. `frontier_justification` becomes required only for a frontier-class selection; `delta_revision` becomes required only for a post-lock revision. `history` accumulates phase reassessments without rewriting completed Run records and becomes required once more than one routed phase has occurred.

### Routing Validation Rules

1. Frontier/Astra escalation fails unless the Frontier Justification contains task-specific evidence and all five Gate elements.
2. After Production Lock, retain or downgrade is the default; escalation or reopened exploration requires new evidence tied to an unmet acceptance criterion.
3. A post-lock revision fails if it does not identify the delta and preserve unrelated locks.
4. A suitable specialised executor is preferred before a stronger general reasoning model; an override requires evidence.
5. Context Budget overflow invokes its declared overflow action and preserves authoritative constraints; it cannot silently truncate context or justify frontier escalation by itself.
6. Phase transitions trigger reassessment, and each reassessment records its cause and next trigger.
7. Capability and executor requirements remain provider-neutral; provider/model names appear only in Run execution records.

### Acceptance Trace

| Phase | Expected routing behaviour | Required evidence or record |
|---|---|---|
| Brainstorm | Use a low-cost capability suitable for divergent volume; bound context and variants. | Five signals, Context Budget, sufficiency rationale, `reassess_on: decision-selection`. |
| Decision | Reassess for synthesis and error cost; increase capability only if the decision requires it. | Phase-change record, selected direction, acceptance criteria and next trigger. |
| Production | Establish Production Lock; prefer the specialist executor and default downgrade for bounded execution. | Locked Decision, executor contract, preserved locks and production capability record. |
| QA | Validate output with the lowest sufficient review capability; create a delta-only revision on failure. | Failed criterion, affected fields, dependencies, preserved locks and revalidation scope. |
| Escalation | Pass Astra Gate only with a complete Frontier Justification. | Lower-capability evidence or defensible risk, alternatives ruled out, bounded frontier scope and exit condition. |
| Downgrade | Return to the lowest sufficient capability when the frontier condition clears or production becomes bounded. | Gate exit condition, new sufficiency rationale and next reassessment trigger. |

### Visual Rendering Capability Routing

Rendering capability is a specialised executor route governed by the same cost-aware, lowest-sufficient-capability policy. The routing decision considers task phase, approved Creative Decision, Hero Constraint, acceptance criteria, cost and time limits, and the capabilities currently available through Provider Adapters.

A renderer is not treated as a permanent final renderer. Discovery and development use the lowest sufficient capability to test the relevant uncertainty. At Decision Lock, when fidelity requirements materially change, or after evidenced validation failure, YCOS performs a Rendering Capability Assessment. The outcome is one of:

- **retain** — the current renderer is sufficient;
- **reconfigure** — the renderer remains sufficient but its inputs or settings require correction;
- **switch** — a different available capability is required;
- **blocked** — no available capability can satisfy the defined acceptance criteria within approved constraints.

Production does not automatically require a more capable renderer. A switch requires evidence that the requirement cannot be met by correcting the Decision, references, Generation Package, adapter configuration or the current renderer within the approved diagnostic budget. Repeated untested retries are prohibited.

Capability requirements are stable, provider-neutral categories such as `specialist_human_photorealism`, `identity_preserving_editing` or `high_precision_typography`. A Run records the actual selected provider, model and settings at execution time. Model names do not become Core architecture.

The assessment must reference the Decision version, define measurable acceptance criteria, record evidence for any insufficiency finding, record the routing outcome, and identify the approved Scene Locks and permitted variance. A renderer transition carries the approved Decision and explicit reference manifest into the Generation Package; post-render validation verifies that the locks were actually preserved.

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
11. Renderer selection is evidence-based and provider-neutral.
12. A renderer transition cannot silently alter approved Scene Locks.
13. Frontier capability requires an evidenced Frontier Justification and a bounded exit condition.
14. Production Lock defaults to downgrade and delta-only revision.
15. Specialist execution is preferred before escalating general reasoning capability.
16. Context Budget overflow preserves authoritative constraints and follows an explicit overflow action.
