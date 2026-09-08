# CORR-03 — Model Artifact and Versioning Contract

DOCUMENTATION STATUS: DATA / GOVERNANCE REQUIREMENT

Each completion artifact contains or immutably references: `ModelVersion`, family, training interval/cutoff, dataset manifest/hash, feature and label schema, target and resolution policy, supported strategy/mode/q/market/route/infra scope, fallback hierarchy, configuration/hyperparameters, calibration state, temporal OOS report, OOD policy, runtime evidence, dependency versions and promotion/demotion state.

Artifacts are immutable and locally resolvable by `RunManifest`/`DecisionTrace`. Training/recalibration happens offline. A candidate cannot overwrite the Champion or silently change live weights; promotion creates a new explicit capability/version and rollback retains lineage. Schema/label/feature/exchange/infra changes trigger compatibility review and revalidation.

Missing/incompatible artifact produces invalid/OOD/no-influence behavior under Simulator/Risk policy, never permissive authority.
