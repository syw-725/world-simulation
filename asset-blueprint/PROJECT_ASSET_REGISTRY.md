# Project Asset Registry Boundary

## Purpose

The Project Asset Registry is the Project-level operational index of assets available to one YCOS Project. It extends Project tooling; it is not a separate Asset OS, a global asset library or a replacement for the [Asset Blueprint Protocol](ASSET_BLUEPRINT_PROTOCOL.md).

```text
Project Asset Registry
= what assets exist in this Project and where their authoritative records are

Asset Blueprint
= what a persistent asset is and how its identity is protected

Asset Resolver
= resolve an asset_id into the exact approved Project configuration
  needed by one creative task or Generation Package
```

## Authority and Identity

Asset Blueprint remains authoritative for Asset Version, Permanent Asset Locks, Controlled Variations, approval and lifecycle meaning. The Registry records a stable Project-scoped `asset_id`, type, role, lifecycle status, Blueprint location, selected Asset Version, optional default Controlled Variant and approved reference locations. Filenames and display names are never identity.

The Registry is Project-local. It cannot discover assets across repositories, index other Projects or write to YCOS Core. Registry paths are explicit, relative Project paths. Absolute, escaping, missing and symlinked paths fail closed.

Supported Project asset types are character, product, environment, prop, wardrobe, vehicle, packaging, logo, food, location and other.

## Resolver Contract

The Project Asset Resolver:

1. reads one canonical Project Registry and rejects duplicate or unknown IDs;
2. resolves only an explicitly requested `asset_id`;
3. validates asset type and active lifecycle status;
4. resolves the declared Blueprint and exact Asset Version;
5. validates an explicitly selected Controlled Variant;
6. keeps Temporary State in the task configuration and never writes it into the Blueprint;
7. preserves the distinction between Permanent Asset Locks, Controlled Variations, Temporary State and Scene Locks;
8. fails closed for missing, deprecated, archived, incompatible or unresolved required assets; and
9. returns a minimum execution view rather than the full Blueprint.

The minimum execution view may contain asset identity, type, resolved version and variant, approved Permanent Asset Locks, task-specific Temporary State and only explicitly selected approved references. It excludes full Blueprints, private rationale, internal history, unused references and unrelated Registry entries.

Scene Locks govern the current Project world. They may coexist with Permanent Asset Locks but may not overwrite them. A conflicting value blocks resolution until deliberately reconciled through the existing Asset Blueprint change rules.

## Semantic Asset Selection

New Project work selects assets semantically:

```yaml
assets:
  required:
    - asset_id: PROD-001
      asset_version: "1.0"
      controlled_variant: null
      temporary_state:
        orientation: three-quarter
        wetness: dry
      references:
        - references/product-approved.png
```

Temporary State is part of the Project task configuration. It never changes the Registry or Blueprint.

Legacy raw-path selections may remain supported only as an explicit compatibility path when the path is a safe, unambiguous Project file. Project tooling must not infer an `asset_id`, Asset Version or Blueprint identity from its filename. New and migrated Projects should use semantic selections.

## External Provider Boundary

Resolution occurs inside YCOS before Generation Package compilation. Providers receive only the selected minimum asset execution view and the exact selected reference allowlist. Registries, complete Blueprints, unrelated assets, rationale and Project history do not cross the External Provider Boundary.
