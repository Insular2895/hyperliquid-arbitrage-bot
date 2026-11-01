# 10 — Drift and Research Triggers

`DOCUMENTATION STATUS: PROPOSED F2 REVIEW CANDIDATE / AWAITING HUMAN REVIEW`

`CAPABILITY STATUS: FUTURE SPECIFIED / LAST-LAYER ACTIVATION / NOT ACTIVE`

Strategy drift is evidence that a previously supported artifact or scope may no longer be supported. It is not permission for autonomous adaptation.

Typed classes are `INPUT_DATA`, `FEATURE_SUPPORT`, `MARKET_REGIME`, `EXECUTION_COMPLETION`, `CALIBRATION`, `ECONOMIC`, `INFRASTRUCTURE`, `SCHEMA_EXTERNAL_FACT`, and `OPERATIONAL`. A signal identifies the detector/version, population, baseline/window, minimum support, statistic/uncertainty, hysteresis, severity, affected artifacts and evidence links.

Interpretable health observables remain separate rather than collapsed into a generic score: Opportunity count/frequency/edge/lifetime/correction speed; route/market distribution; BBO-to-L2 and candidate-to-attempt funnels; zero/partial/full/Recovery outcomes; PnL/slippage/fees/priority; participant cancellation/refill; feature/regime/support/OOD/calibration; `Q_validated` support; latency and `InfraProfile` drift. Predicted distributions are compared with recent reconciled actual coverage, bias, completion, tails and economics.

Thresholds require historical calibration and false-positive/false-negative analysis. Insufficient support yields `UNAVAILABLE` or review, not a confident alert. Hysteresis and recovery windows prevent oscillating promotion/demotion.

Allowed consequences are alert/evidence creation, revalidation, scope contraction, q/capital contraction through existing Risk authority, safe demotion to a supported artifact, NON-READY, incident or a new research hypothesis. A detector cannot update model weights/features/parameters, raise limits, promote a challenger or resume Live.

Three research dispositions remain distinct: parameter drift may propose offline recalibration of the same family; regime change may evaluate an already validated scoped artifact; structural change opens a new hypothesis/family. All re-enter the full evidence chain. Periodic cadence stays calibrated; event-driven triggers include external-rule/node/network/liquidity/listing changes, persistent outcome degradation and incidents/postmortems.

Demotion preserves one execution owner, stops new risk where required, lets ESM/Recovery/Reconciliation resolve outstanding truth, records the event and uses a declared fallback. Contradictory actual outcomes dominate simulated expectations.

This capability is implemented last: only after the baseline, deterministic reporting, StrategySpec lineage, temporal OOS, Champion/Challenger and safe rollback exist. Initial production artifacts do not self-learn online.

Hard safety monitors may stop new risk immediately under the Risk Constitution. Weak statistical strategy drift normally creates research/demotion evidence and never overrides hard Risk semantics. A single bad day is not automatically a new regime; minimum samples, economic materiality and hysteresis apply.

## Immutable StrategyVersion lifecycle

Drift never edits a deployed artifact. The exact observed `StrategyVersion`, detector/window and
external-fact/fee/feed/model versions remain linked to the evidence. A proposed change creates a new
`HYP-*`/`EXP-*` and, if material, a candidate immutable version with explicit parent and evidence
transfer limits. Failed, demoted, retired and superseded versions remain queryable.

### D9 — Drift to candidate v2 and human-controlled progression

```text
Validated StrategyVersion v1
             |
             v
reconciled Actual Evidence + support/external-fact versions
             |
             v
       Drift Detection
             |
     +-------+--------------------+
     |                            |
insufficient support         hard safety issue
     |                            |
     v                            v
REVIEW / UNAVAILABLE       canonical Risk action
     |                            |
     +-------------+--------------+
                   |
                     v
        Research Trigger (if warranted)
                     |
                     v
              new HYP-* / EXP-*
                     |
                     v
       offline Research / Falsifier
                     |
                     v
       candidate StrategyVersion v2
                     |
                     v
 independent Validation / OOS / T2 / holdout
                     |
                     v
        human-controlled promotion pathway

v1 is never mutated; v2 never self-promotes.
```

Read top-to-bottom: reconciled actual evidence may reveal unsupported behavior; safety remains with
Risk, while research creates new immutable lineage and can only forward a validated candidate to a
human-controlled pathway.

Contract — **Inputs:** exact v1, reconciled actual evidence, detector/support and dated fee/feed/
external-fact versions. **Operations:** typed drift evaluation, support check, Risk escalation or
research trigger, frozen offline experiment and independent validation. **Outputs:** alert,
evidence, scope contraction/demotion/retirement or non-authorizing v2 candidate. **Canonical
authority:** Execution/Reconciliation for actual facts, Risk for safety, Validation for evidence,
humans for promotion. **Failure/uncertainty:** insufficient samples/support are `UNAVAILABLE`/
review; contradictory actual outcomes dominate simulations; no silent refit. **Activation timing:**
last-layer capability after baseline, reporting, lineage, Champion/Challenger and rollback exist.

External fee, feed, metadata, schema or market-rule changes do not rewrite historical results. They
create dated version boundaries, affected-artifact queries and revalidation triggers. Safe
consequences may contract or demote scope; recovered health cannot auto-resume or auto-promote.

Detector thresholds, materiality, hysteresis, re-entry policy and version evidence-transfer rules
remain `CALIBRATED / HUMAN_DECISION_REQUIRED`. Safe default is alert/review or conservative scope
contraction through existing authority, never online learning or automatic v2 activation.
