# Architecture Gap Register

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

## PASS 13 architecture-only closures

| Gap | Result | Architecture closure | Domain truth changed? |
|---|---|---|---|
| `ROADMAP_CROSS_DOMAIN_GAP-001` concrete topology | RESOLVED | one modular Rust process, one ordered logical writer, bounded async/offline workers; no crate/thread invention | NO |
| `ROADMAP_CROSS_DOMAIN_GAP-003` Deployment/Operations placement | RESOLVED | cross-cutting prerequisite/control-plane workstream across 26 phases; phases not renumbered | NO |
| `ROADMAP_CROSS_DOMAIN_GAP-004` optional TTT/model edge | RESOLVED | dependency is declared by exact CapabilityManifest; basic TTT is not universally model-gated | NO |
| Sizing↔Simulator call ambiguity | RESOLVED | Simulator evaluates declared q candidates; Sizer selects returned curve | NO |
| Atlas↔Capital feedback | RESOLVED | only delayed point-in-time AtlasVersion feedback; decision pins current version | NO |
| Recovery↔Execution loop | RESOLVED | Recovery proposes; Risk authorizes; Execution alone applies new plan | NO |

## Routed to PASS 14

| Gap ID | Ambiguity | Existing truth / why not silently closed | Required PASS 14 action | Blocking now? |
|---|---|---|---|---|
| `ARCH-GAP-001` | Final serialized integration for phase/evidence artifacts (`ROADMAP_CROSS_DOMAIN_GAP-002`) | Producers/consumers are known; exact Data-governed envelope/compatibility fields remain distributed | Crosscheck `CapabilityManifest`, Evidence/Model/Atlas/phase reports against frozen Data contracts and approve schema owner | No for documentation; yes before implementation claim |
| `ARCH-GAP-002` | Accounting has no standalone V2 master | QF-105–110 and Execution/Inventory/Data define semantics; architecture assigns logical Accounting owner but must not create domain truth | Confirm authoritative master placement and serialized accounting boundary | No |
| `ARCH-GAP-003` | Exact consolidated health-state vocabulary across Risk/Infra/Operations | Infra master uses HEALTHY/DEGRADED/UNSAFE; other closure material may express critical/severity separately | Verify enums versus alert severity and preserve semantic layers | No; values remain typed/calibrated |
| `ARCH-GAP-004` | Position Sizer organizational boundary | Inventory/Capital owns economic q; Risk owns ceilings/final permission; some prose says sizing “inside Risk” | Confirm module/API ownership without changing staged permission | No |

Unowned canonical state: **0**. Duplicate logical state owners: **0**. Synchronous dependency cycles: **0**. No RunMode bypass or unversioned model feedback was found in the assembled architecture.
