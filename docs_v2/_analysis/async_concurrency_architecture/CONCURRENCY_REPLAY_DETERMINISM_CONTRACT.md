# Concurrency Replay Determinism Contract

`DOCUMENTATION STATUS: AWAITING FINAL HUMAN REVIEW`

Canonical property:

```text
DecisionTrace = F(
  OrderedEvents,
  ResolvedConfig,
  ModelArtifacts,
  FormulaVersion,
  Seed
)
```

It is not a function of worker thread count, task polling, OS scheduling, queue interleaving, hash-map iteration, completion order or host speed. A scheduling policy that intentionally changes which complete candidate set is eligible is explicit, versioned and compared as a policy; inside that policy, identical inputs still reproduce.

## Commit protocol

1. Replay emits the recorded ordered input schedule through the same Core reducers.
2. Worker jobs have deterministic identity from ordered cursor, family, generation and complete input fingerprint.
3. Results are collected by identity, never arrival position.
4. `BATCH_SELECT` closes by its recorded/versioned completion/deadline rule. `EARLY_COMMIT` uses its declared deterministic priority/admissibility evidence. First-worker-wins is invalid.
5. Current version revalidation, Risk, Reservation and commit use the same ordered logic.
6. Traces record worker timing/disposition separately from economic order.

## Scheduler-independence fixtures

| ID | Perturbation | Required result |
|---|---|---|
| CT-001 | results A then B versus B then A | same decision under same declared policy |
| CT-002 | one result uses stale BookVersion | stale discarded; no stale commit |
| CT-003 | worker never returns | bounded fallback/reject; Core continues |
| CT-004 | Recorder P2/P3 pressure | same canonical decision; missingness visible |
| CT-005 | exporter stalls | Core/DecisionTrace unaffected |
| CT-006 | ACK delayed | coordinator processes other events; order pending/UNKNOWN by timers |
| CT-007 | fill observed before ACK | fill applies once and drives state |
| CT-008 | fill races cancel | ordered evidence produces valid race outcome |
| CT-009 | reconciliation HTTP is slow | NON-READY/UNKNOWN state advances; event loop remains live |
| CT-010 | opportunity worker flood while fill arrives | fill/safety processing wins; no starvation |
| CT-011 | worker panic | scoped loss/fallback; no owner loss |
| CT-012 | archive unavailable | local evidence/health state; no decision block |
| CT-013 | market ingress gap | Book invalid/resync; no silent continuation |
| CT-014 | two-vCPU oversubscription treatment | same semantics; pressure/tails measured |
| CT-015 | varied worker count, queue and scheduler seed | same trace for transparent configuration |

## Required assertions

- exact ordered decisions/intents/state transitions/Risk decisions and trace hash for transparent scheduling changes;
- canonical sorting/tie-breaks for routes, q, allocations and results;
- no dependence on unordered collection iteration or floating completion time;
- canceled/late/duplicate results retain deterministic dispositions without economic effect;
- Replay mode does not need real external services; transports and clocks provide recorded/simulated events.
