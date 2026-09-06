# Status Consistency Matrix

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

| Status family | Canonical values / rule | Must not be confused with | Result |
|---|---|---|---|
| documentation | `REBUILD IN PROGRESS` | implementation approval | CONSISTENT |
| requirement provenance | `LOCKED`, `CALIBRATED`, `LEARNED`, `RESEARCH`, `FUTURE`, `SOURCE_SNAPSHOT`, `EXTERNAL_REVALIDATION`, `OPEN`, `SUPERSEDED`, `REJECTED` | capability maturity | CONSISTENT |
| maturity | M0 SPECIFIED → M1 UNIT VALIDATED → M2 REPLAY VALIDATED → M3 SHADOW VALIDATED → M4 MICRO-LIVE VALIDATED → M5 LIVE VALIDATED | whole-project status, runtime state | CONSISTENT |
| effective capability | intersection of compiled/configured/licensed/channel/validated/readiness/Risk | any one input alone | CONSISTENT |
| EngineState | `BOOTING`, `SYNCING`, `RECONCILING`, `READY`, `DEGRADED`, `RECOVERY_ONLY`, `HALTED`, `SHUTTING_DOWN`, `STOPPED` | liveness or `InfraState` | CONSISTENT |
| OrderState | exact 14-state lifecycle ending at `TERMINAL_RECONCILED` | transport acknowledgement or fill alone | CONSISTENT |
| ReconciliationState | requested/fetching/comparing/resolving/consistent/unresolved | startup readiness | CONSISTENT |
| `InfraState` | `HEALTHY`, `DEGRADED`, `UNSAFE` | P0–P3 alert severity | CONSISTENT AFTER FIX |
| data quality | valid/invalid/low-fidelity plus explicit gaps/unknown | healthy or zero | CONSISTENT |
| simulation confidence | `HIGH`, `MEDIUM`, `LOW`, `REJECT` from gates | arbitrary weighted score or Risk allow | CONSISTENT |
| HWC | `HOT`, `WARM`, `COLD` compute/relevance | Risk-safe/unsafe | CONSISTENT |
| release channel | `DEVELOPMENT`, `CANDIDATE`, `STABLE` | Live permission | CONSISTENT |
| incident severity | P0–P3 | infrastructure enum | CONSISTENT AFTER FIX |

All prior `CONFLICT-001..126` retain resolved status; PASS14 `CONFLICT-127..128` are resolved. Open/calibrated/external states are not misreported as contradictions.
