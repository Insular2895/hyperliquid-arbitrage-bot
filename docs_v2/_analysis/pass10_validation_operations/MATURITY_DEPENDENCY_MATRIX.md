# Maturity Dependency Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Capability | Critical dependencies | Maximum without dependency proof | Required promotion join |
|---|---|---|---|
| Direct/OWA/Triangle detection | metadata, books, Graph, NetConvert, fee/precision formulas, clock | minimum dependency maturity | exact direction/closure, point-in-time and golden economics |
| Participant survival | recorder, labels/censoring, point-in-time features, model registry | M2 before live observation | temporal OOS, calibration, baseline and runtime |
| Counterfactual simulation | Replay, exchange emulator, participant forecasts, RNG/versioning | minimum fidelity/dependency level | calibrated distribution, OOD and predicted/actual evidence |
| Position sizing / Q_validated | execution forecast, Risk, inventory/capital, Atlas support | zero outside common support | size-curve evidence and all-gates proof |
| Taker execution | signer/transport, account truth, state machines, Risk, reconciliation | no real capital before M4 | partial/UNKNOWN/recovery and actual-fill evidence |
| Maker modes | taker/recovery plus queue/fill/adverse-selection models | disabled until dependencies qualify | resting/cancel-race/queue calibration by mode |
| Bridge | Graph reachability, inventory, terminal viability, execution/recovery | no capital relocation | compare all paths and STAY; realized relocation/exit evidence |
| Live release | artifact integrity, runtime hardening, config/schema compatibility, startup/readiness | non-Live channel only | release test evidence + CapabilityManifest |
| Infrastructure profile | benchmark, clock, feeds, resources, recorder, security profile | Shadow/diagnostic only | comparable distributions, stability and economic gate |
| Capital/market expansion | Q_validated, model/simulator support, Risk, operations health | previous validated band/scope | next-band evidence; no inheritance from capital balance |

Dependency regression makes the dependent capability ineligible even if its own historical report passed. Recovery/cancel/reconciliation capability remains available where safe while new risk is removed.
