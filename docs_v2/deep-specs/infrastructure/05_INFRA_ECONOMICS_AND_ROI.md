# 05 — Infrastructure Economics and ROI

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

## Authority

SRC-004 Formula Book entries QF-084 through QF-093 are canonical. This spec explains their infrastructure use without modifying them. Formula discrepancies or future changes belong to PASS 11.

## Objective hierarchy

1. Respect Risk and execution permissions.
2. Maximize robust absolute `NetPnL` under comparable strategy/opportunity/capital assumptions.
3. Use `NetUpgradeValue`, uncertainty and validation to decide transitions.
4. Use `InfraROI` and `InfraEfficiency` as diagnostics under their defined domains, never as substitutes for absolute net value.

Technical speed is an input. It is not the objective.

## QF-084 — Infrastructure latency

```text
L_total = L_feed + L_compute + L_sign + L_send + L_exchange

L_compute =
  L_decode + L_book + L_route + L_simulation + L_risk + L_decision
```

The decomposition distinguishes infrastructure-controlled and exchange/external components while retaining end-to-end consequences. Instrumentation can use finer stages only with a documented mapping and no double counting.

## QF-085 — Capture probability

```text
P_capture,s = E_{L_s}[S(L_s)]
```

`L_s` is the measured latency distribution under scenario/infrastructure `s`; `S(t)` is the opportunity survival function. A faster median does not alone establish a higher capture probability because tails and survival shape matter.

PASS 01 supplies `L_s`. PASS 02 owns detailed `S(t)`/participant competition modeling.

## QF-086 — Incremental gross PnL

```text
ΔGrossPnL = GrossPnL_candidate - GrossPnL_current
```

The comparison uses the same opportunity universe, strategy and capital assumptions. If allocation or opportunity assignment differs, the experiment must explicitly correct/design for it. `ΔGrossPnL` is not a comparison of unrelated calendar periods without controls.

## QF-087 — Incremental cost

```text
ΔCost = Cost_candidate - Cost_current
```

Cost includes the infrastructure costs relevant to the comparison under a declared horizon and billing basis. One-time research rental can be separated from recurring production cost, but neither is silently omitted when material.

## QF-088 — Net upgrade value

```text
NetUpgradeValue = ΔGrossPnL - ΔCost
```

`REQ-FORMULA-0103` was recovered into the Infrastructure index during PASS 01. Positive point estimate alone is insufficient; QF-091 applies uncertainty.

## QF-089 — InfraROI

```text
InfraROI = ΔGrossPnL / ΔCost
```

Only defined for `ΔCost > 0`. When `ΔCost <= 0`, compare `NetPnL` directly; do not create misleading negative/undefined ratios. ROI does not authorize a transition by itself.

## QF-090 — NetPnL

```text
NetPnL_s =
  GrossTradingPnL_s
  - TradingCosts_s
  - InfrastructureCost_s
```

Trading costs must not be subtracted twice if gross/realized fields already embed some cost. The accounting schema and comparison report state the exact convention.

## QF-091 — Lower-confidence-bound upgrade gate

```text
LCB_alpha(ΔGrossPnL) > SF × ΔCost
```

`alpha`, safety factor `SF`, estimator and dependence treatment are learned/calibrated under `OPEN-005`. The invariant is that a point estimate is insufficient and the gate must be conservative enough for decision risk.

The gate is evaluated only on valid/comparable evidence and does not override Risk or Validation.

## QF-092 — Infrastructure efficiency

```text
InfraEfficiency = NetPnL / InfraCost
```

This is diagnostic. Maximizing the ratio can select a tiny cheap machine with lower absolute `NetPnL`, so the primary objective remains absolute robust net value.

## QF-093 — CaptureRatio

Preferred aggregate form:

```text
CaptureRatio =
  sum(RealizedPnL)
  / sum(ExpectedExecutablePnL)
```

The exact Formula Book definition governs field eligibility/zero-denominator handling. Never use a naïve unweighted average of per-opportunity ratios. `REQ-FORMULA-0108` was recovered into the Infrastructure index during PASS 01.

CaptureRatio is diagnostic of capture quality and can help detect infrastructure limitation. It is not attributed to infrastructure without counterfactual/control evidence.

## Opportunity Survival interface

Infrastructure emits latency distributions, event/decision times, feed health and candidate identity. The participant/survival domain returns model/versioned `S(t)` or equivalent capture estimates and uncertainty. PASS 01 does not duplicate the participant model or lock survival coefficients.

## InfraLostPnL

`InfraLostPnL` estimates PnL not captured because of infrastructure, including late feed, network delay, compute latency, scheduler jitter, feed degradation, reconnect or outage.

An `InfraLostPnLRecord` retains at least:

- opportunity/event/route identity;
- current `InfraInstanceId` and run/build/config;
- observed infrastructure state and latency components;
- expected executable PnL baseline and realized outcome;
- cause candidates and attribution order;
- counterfactual/candidate assumption;
- estimator/model/data version;
- estimate, uncertainty/confidence and validity flags.

When causes coexist, use an approved sequential marginal attribution or another method that prevents double counting. Total losses must not be independently charged in full to feed, CPU, network and outage.

## RecoverablePnL

`RecoverablePnL` is the portion of estimated InfraLostPnL defensibly expected to be recovered by a specific candidate under comparable conditions. It is candidate-, horizon- and model-specific.

```text
total modeled loss
!=
recoverable loss
!=
guaranteed future PnL
```

The estimator remains `CALIBRATED / MODEL_DERIVED` until validated.

## Upgrade pipeline

1. Measure current infrastructure and `InfraLostPnL` with provenance.
2. Determine whether infrastructure is actually limiting rather than strategy, liquidity, fees, Risk or execution logic.
3. Rent a candidate for a controlled comparable benchmark.
4. Reject if technical evidence is invalid or not better on the relevant dimensions.
5. Run shadow/counterfactual evaluation and estimate `ΔGrossPnL`.
6. Quantify uncertainty and apply QF-091 against `ΔCost`.
7. Confirm positive robust `NetUpgradeValue`/`NetPnL` and acceptable Risk/stability.
8. Run the required micro-live/validation stage.
9. Change production only after operator approval and Deployment/Validation gates.

The approximate 72-hour screening duration is calibratable and does not replace sample/regime sufficiency.

## Downgrade pipeline

Evaluate the current premium infrastructure as the candidate advantage over a cheaper validated baseline. If the robust incremental gross value is below incremental cost, or if cheaper infrastructure yields higher acceptable `NetPnL`, downgrade.

Sunk rent, setup effort and historical reasons for upgrade do not change the forward comparison. Reliability and risk costs still enter; cheapest is not automatically best.

## Capital is not the trigger

```text
more capital != automatic infrastructure upgrade
```

Capital may affect opportunity capacity/exposure, but transition evidence is validated capture limitation, opportunity density, InfraLostPnL, RecoverablePnL, stability/risk and incremental economics. No universal capital-to-server bands are canonical.

## A/B and shadow validity

The same opportunity must not be executed concurrently from two servers when that creates self-competition. Technical shadow can observe both. Live treatment uses an approved alternating/randomized/assigned design, preserves comparable assumptions and records assignment/selection bias.

Counterfactual output is not “the exact alternate universe.” It is a calibrated estimate with version, assumptions and uncertainty. Replay/Simulation authority governs deeper counterfactual mechanics.

## Infrastructure technical heuristic

The historical weighted technical score can screen candidates. It cannot replace QF-086–QF-092, because score points do not directly equal economic value and weights are a research heuristic.

## Illustrative example — not a decision

`ILLUSTRATIVE`: if a candidate costs EUR 60 more over the evaluation horizon and modeled incremental gross PnL is EUR 100, point `NetUpgradeValue` is EUR 40. The upgrade still fails if the chosen lower confidence bound does not clear `SF × EUR 60`, or if Risk/Validation evidence is insufficient. These numbers are not project thresholds.

## Reporting contract

An upgrade/downgrade report states:

- current/candidate identities and horizon;
- comparable opportunity/strategy/capital assumptions;
- technical distributions and invalid intervals;
- CaptureRatio and survival-model version;
- InfraLostPnL/RecoverablePnL estimator and uncertainty;
- `ΔGrossPnL`, `ΔCost`, `NetUpgradeValue`, eligible `InfraROI`, both `NetPnL`, diagnostic `InfraEfficiency`;
- LCB method, `alpha`, `SF` and result;
- risk/stability incidents;
- shadow/micro-live/validation evidence;
- decision owner and explicit result: keep, upgrade, downgrade, reject or gather more evidence.

## Open items

- `OPEN-001`: actual provider ranking;
- `OPEN-005`: `alpha`, `SF` and LCB method;
- InfraLostPnL/RecoverablePnL estimator calibration;
- live A/B assignment design;
- opportunity survival model: PASS 02.

## Requirement anchors

QF-084–QF-093, `REQ-INFRA-0075`–`REQ-INFRA-0087`, `REQ-CAP-0021`, `REQ-CAP-0022`, `REQ-INFRA-0092`, `REQ-INFRA-0096`–`REQ-INFRA-0098`, and their Risk/Data/Validation dependencies in the PASS 01 ledger.
