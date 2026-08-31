# PASS 01 — Infrastructure Legacy Comparison

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

## Method

The six legacy files were read only after the source-derived V2 master and deep specs existed. Legacy content was used as a no-loss check, never as design authority. No file under `docs/**` was modified.

Reviewed files:

- `docs/13_INFRASTRUCTURE.md`;
- `docs/specs/InfrastructureBenchmark.md`;
- `docs/specs/InfrastructureMonitor.md`;
- `docs/specs/InfrastructureROI.md`;
- `docs/specs/Deployment.md`;
- `docs/18_OPERATIONS_AND_MONITORING.md`.

## Classification summary

| Classification | Result |
|---|---:|
| Correct and recovered | 29 concept groups |
| Correct but missing from V2 | 0 material groups after comparison |
| Over-compressed in legacy | 18 material groups |
| Superseded/needs status correction | 2 groups |
| Legacy-untraced | 0 accepted requirements |
| Contradicted | 0 newly discovered conflicts |

## Comparison

| Legacy material | Classification | PASS 01 treatment |
|---|---|---|
| Maximize safe/reproducible NetPnL, not server prestige | Correct and recovered | Master objective and economics deep spec |
| One VPS/client, public feed, node-compatible but not required | Correct and recovered | Master baseline; deep specs 01 and 06 |
| Tokyo as revalidated hypothesis | Correct but over-compressed | Expanded into `TOKYO_FIRST`, provider/region agnosticism and `OPEN-002` |
| QF-084 latency path and P50/P95/P99/P99.9 | Correct but over-compressed | Exact QF closure plus twelve-benchmark instrumentation |
| Same universe/config/capital and healthy clocks | Correct but over-compressed | RunManifest, comparability and invalidity contracts |
| CPU steal/scheduler, memory, disk/recorder, loss, reconnect | Correct but over-compressed | Individual benchmark purposes, measurements, artifacts and decisions |
| `hl-infra-benchmark` does not trade | Correct and recovered | Tool remains conceptual/offline/non-executing |
| QF-085–QF-093 and LCB gate | Correct but over-compressed | Exact formulas, validity domains and report contract; recovered QF-088/QF-093 tags |
| Downscale when cheaper robust NetPnL wins | Correct and recovered | Symmetric downgrade pipeline |
| Optimizations only after profiling/risk review | Correct and recovered | Untuned-first rule and future tuning candidates |
| No illustrative microsecond target as locked SLO | Correct and recovered | `CONFLICT-004` resolution and calibrated KPI status |
| Restart/health/readiness, clock/disk/recovery/rollback | Correct but over-compressed | Cold recovery, InfraState, machine revalidation and failure tests |
| Raw benchmark distributions/confidence | Correct and recovered | Run artifacts and common statistical contract |
| Benchmark must not disturb Live | Correct and recovered | Read-only/safe context and explicit A/B constraints |
| InfrastructureMonitor nonblocking/bounded metrics | Correct and recovered | Monitor boundary and Recorder/hot-path contract |
| Liveness ≠ readiness ≠ trading health | Correct and recovered | InfraState/Risk and diagnostic separation |
| Security/reliability can veto positive ROI | Correct and recovered | Risk/Validation preconditions in economics |
| Deployment image/config/secrets/volumes/update/rollback | Correct cross-domain material | Referenced to SRC-006 authority; only infra preflight/recovery interface reproduced |
| No `latest`, privileged container or Docker socket | Correct deployment detail | Not promoted into Infrastructure master; remains Deployment pass responsibility |
| One writer/account and no auto-Live | Correct and recovered at boundary | Client isolation, single-writer and explicit validation/approval |
| License never blocks recovery | Correct deployment detail | Kept outside PASS 01 domain; future Deployment/License pass |
| Market/data/decision/execution/risk/model/system metric catalog | Correct but cross-domain | Infrastructure subset defined; complete catalog remains PASS 10 |
| P0–P3 alert classes and runbooks | Correct but cross-domain | Infrastructure alert inputs/actions linked; full policy remains PASS 10 |
| Incident package and chain of custody | Correct but cross-domain | Not duplicated; Operations/Data authority retained |
| Availability alone is insufficient | Correct and recovered | Multi-dimensional health, stability and economic evidence |
| Safe shutdown sequence | Correct but cross-domain | Referenced to Execution/Operations; not redefined in PASS 01 |
| Archive failure need not always stop trading | Requires domain authority/context | PASS 01 does not generalize it; Risk/Recorder/Data decides when auditability loss forbids new risk |
| NTP wording | Superseded/clarified | Initial direction is chrony; contract uses synchronized wall clock plus measured uncertainty |
| Tokyo “to revalidate” without first-direction status | Superseded/clarified | Tokyo is explicitly the first validation direction but not eternal |

## Major legacy omissions recovered from sources

The legacy set did not contain enough detail to answer the PASS 01 success test. V2 recovers:

- exact historical snapshots and benchmark questions for TradingFX, Akamai/Linode, Kamatera, Lightsail, Sakura and Cherry;
- explicit Wave 1, Wave 2 and much-later gates;
- 72-hour screening, optional seven-day finalist phase and EUR 50–100 research budget;
- all twelve benchmark contracts, including First Market Data Arrival, Feed Age, `TimeToHealthyFeed`, scheduler/contention, RecorderPenalty, RAM and Docker overhead;
- `clock_offset`, `clock_uncertainty`, `root_dispersion`, event identity and inconclusive-clock treatment;
- the production working disk versus R&D/archive storage distinction;
- exact QF-084–QF-093 interpretations and formula validity conditions;
- first-class InfraLostPnL/RecoverablePnL records, attribution and uncertainty;
- full upgrade and downgrade pipelines;
- capital-not-trigger and no capital-to-server bands;
- public-feed limitation evidence and node escalation/economics;
- client diagnostic, material `InfraInstanceId` revalidation and recommendation boundaries;
- cold-recovery-first and future standby/split-brain gates.

## Legacy-only untraced material

No legacy-only item was accepted into PASS 01 without original-source support. Deployment/security details such as image tag/privilege/socket policy, licensing behaviour and full Operations incident/runbook content remain routed to their domain passes; they are not classified as missing Infrastructure truth.

## Conclusion

Legacy Infrastructure was directionally strong but deliberately compressed. V2 preserves its correct principles, corrects ambiguous status wording, and restores the provider, measurement, economic, node and client-operational detail required for implementation planning without copying legacy-only authority.
