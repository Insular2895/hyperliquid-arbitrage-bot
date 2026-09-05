# PASS 10 Legacy Comparison

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

Legacy was inspected only after source-first reconstruction. Files compared: `docs/16_VALIDATION_MATRIX.md`, `docs/18_OPERATIONS_AND_MONITORING.md`, and the legacy `ReplayEngine`, `InfrastructureMonitor`, and `ShadowBook` specs. Legacy remains read-only reference.

| Legacy concept | Source-first result |
|---|---|
| compact M0–M5 and domain matrix | recovered and expanded with exact dependency/scope/promotion/demotion semantics |
| test/fault list | recovered and expanded to explicit oracles, economic state, permissions, evidence and reconciliation |
| capability manifest | corrected to the source-backed mandatory field set; extra identities linked rather than invented as mandatory |
| metric families | recovered with validity, distributions, cardinality and non-blocking export requirements |
| P0–P3 alerts | recovered as normalized severity; numeric triggers retained as calibrated |
| seven short runbooks | recovered and expanded to fifteen indexed scenarios and restart/resume proof |
| incident package/chain | recovered with canonical timeline, manifests/hashes, local redaction and client-controlled export |
| SLO/uptime distinction | recovered and expanded into ten trading-system SLO classes |
| Replay exact/fast/no-lookahead | recovered under Data determinism authority |
| InfrastructureMonitor loss/cardinality/clock risks | recovered in metric validity, bounded labels and non-blocking/fail-visible contracts |
| ShadowBook mechanics | retained under Simulator; distinguished from Shadow run mode |

Legacy omissions recovered by PASS10 include: reversible M5; source-exact maturity names; exact dependency ceiling; Shadow limitations; Micro-live predicted/actual joins; Champion/Challenger/OOD/drift gates; Q_validated shrink; release/change revalidation; locked versus calibrated alert behavior; readiness versus liveness; drill evidence; incident-based demotion; and explicit PASS10/PASS12 separation.

No source-backed item was removed because legacy omitted it. No legacy-only implementation/vendor choice was promoted.
