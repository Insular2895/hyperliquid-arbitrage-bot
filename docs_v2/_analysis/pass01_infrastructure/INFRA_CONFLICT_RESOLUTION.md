# PASS 01 — Infrastructure Conflict Resolution

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

## Method

PASS 01 reopened the original locators behind every relevant conflict. Formula, Risk/Data and Deployment/Validation closure sources override exploratory prose in their domains. SRC-008 is the latest detailed Infrastructure synthesis where those closures do not supersede it. Historical alternatives remain traceable and are not silently deleted.

## CONFLICT-002 — Node at launch

- **Earlier position:** node-focused architecture and local order-book-server research in SRC-002/SRC-007 could be read as a launch requirement.
- **Later/closure evidence:** SRC-006 deployment direction and SRC-008 latest infrastructure synthesis specify a lightweight initial VPS using the public feed, while preserving feed abstraction and future node compatibility.
- **Resolution:** `RESOLVED IN PASS 01` — architecture is node-compatible; deployment is public-feed-first; node is not required initially.
- **Future gate:** `OPEN-006` requires current node capabilities, measured public-feed limitation, candidate technical evidence, RecoverablePnL, incremental cost/uncertainty and validation.
- **Canonical targets:** `13_INFRASTRUCTURE.md`; deep spec 06.
- **History retained:** earlier node topology informs the future separate node/trading-machine design only.

## CONFLICT-003 — Production storage size

- **Earlier position:** SRC-003 and other research/Recorder contexts contain comfortable 100–300 GB, 250–500 GB or larger/approximately 1 TB storage examples.
- **Later infrastructure direction:** SRC-008 proposes an approximately 40–100 GB lightweight initial VPS disk.
- **Closure/deployment context:** SRC-005/006 require data integrity, working storage and validation but do not turn one illustrative capacity into a universal invariant.
- **Resolution:** `RESOLVED IN PASS 01` — separate production working storage from research/archive storage. The light VPS disk is an initial calibrated hypothesis; large research/archive capacity is a different role. Final capacities derive from Recorder throughput, retention and recovery evidence (`OPEN-011`).
- **Canonical targets:** master storage distinction; deep specs 01, 03/B10 and 07.
- **No deletion:** both ranges remain as role-specific historical/calibrated guidance.

## CONFLICT-004 — Fixed latency thresholds

- **Earlier position:** sources include illustrative kill thresholds, millisecond budgets and internal compute targets such as P50 approximately 200–300 microseconds or P95 below approximately 500 microseconds.
- **Closure evidence:** SRC-004 formula closure defines decompositions/mechanisms; SRC-005 requires calibrated, versioned parameter provenance and forbids magic numbers.
- **Resolution:** `RESOLVED IN PASS 01` — mechanisms, distributions, safety response and evidence requirements are canonical; exact thresholds/windows are calibrated. Historical figures are KPI hypotheses/examples, not SLOs, guarantees or universal Risk limits.
- **Canonical targets:** master calibrated aspects; deep specs 03, 04 and 07; `OPEN-004`.
- **Superseded item:** the earlier fixed kill-latency proposal represented by `REQ-RISK-0002` remains `SUPERSEDED_CONTEXT` rather than erased.

## CONFLICT-008 — Capital-driven infrastructure

- **Earlier position:** conceptual client/performance tiers could imply that larger capital directly selects a more expensive server.
- **Latest/formula evidence:** SRC-008 explicitly rejects capital as the direct trigger; SRC-004 QF-084–QF-093 governs latency-to-capture and incremental economics.
- **Resolution:** `RESOLVED IN PASS 01` — capital alone never triggers upgrade. A transition requires validated infrastructure limitation, attributable InfraLostPnL/RecoverablePnL, technical improvement, `ΔGrossPnL`, `ΔCost`, uncertainty/LCB, robust net value and validation. Downgrade is symmetric.
- **Canonical targets:** master; deep spec 05.
- **Remaining calibration:** LCB method/parameters remain `OPEN-005`; this does not reopen the capital rule.

## Related formula-index correction

PASS 00 did not tag QF-088 `REQ-FORMULA-0103` and QF-093 `REQ-FORMULA-0108` as Infrastructure-relevant. PASS 01 adds them to the Infrastructure domain index without changing IDs, primary domain or Formula Book authority.

## Outcome

| Conflict | PASS 01 status | Residual open decision |
|---|---|---|
| `CONFLICT-002` | Resolved initial architecture | Node activation and current capabilities (`OPEN-006`) |
| `CONFLICT-003` | Resolved storage roles | Exact working/archive capacities (`OPEN-011`) |
| `CONFLICT-004` | Resolved status of numerical examples | Calibrated health thresholds/windows (`OPEN-004`) |
| `CONFLICT-008` | Resolved decision driver | LCB parameters/method (`OPEN-005`) |

No conflict remains open at the architectural-principle level for PASS 01. The residual items are explicit measurements or future activation decisions.
