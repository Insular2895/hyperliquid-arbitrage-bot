# 03 — Microstructure Features, OFI and Microprice

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

## Role and invariants

Microstructure features describe point-in-time book and flow state for survival, liquidity, maker and cross-market models. No feature is an autonomous trading signal or hard Risk override. Computation is incremental, bounded, versioned and free of future information.

Each snapshot records market, event/as-of time, input sequence/range, feed mode, feature definition/version, window/horizon, freshness and validity. Gap, reorder, stale/crossed book, unknown denominator or feature-schema mismatch invalidates affected values rather than substituting an optimistic zero.

## Queue Imbalance — QF-028

```text
QI = (Q_bid - Q_ask) / (Q_bid + Q_ask)
```

`Q_bid` and `Q_ask` are best-level quantities under the authoritative book units. Denominator zero is invalid. QI lies in `[-1,1]` for non-negative quantities. Its directional relationship to survival, fill or adverse selection is learned, never assumed.

## Multi-Level Imbalance — QF-029

```text
QI_K = [sum_k w_k Q^b_k - sum_k w_k Q^a_k]
       / [sum_k w_k Q^b_k + sum_k w_k Q^a_k]
```

The structure is locked. Depth `K`, weights and normalization/support are calibrated. An equal-weight baseline may be challenged, but learned weights require temporal validation.

## True event-level OFI — QF-030..032

For ordered top-of-book events `n`:

```text
e^b_n = 1[P^b_n >= P^b_{n-1}] Q^b_n
        - 1[P^b_n <= P^b_{n-1}] Q^b_{n-1}                 QF-030

e^a_n = 1[P^a_n <= P^a_{n-1}] Q^a_n
        - 1[P^a_n >= P^a_{n-1}] Q^a_{n-1}                 QF-031

OFI_n = e^b_n - e^a_n
OFI_W = sum_{n in W} OFI_n                                QF-032
```

The equality cases are intentional and must be tested. Event OFI represents market orders, limit additions and cancellations through ordered book changes; executed volume alone is insufficient.

## Snapshot OFI proxy

When only snapshots are observable, exact intervening add/cancel/modify order is unknown. A difference-based `SnapshotOFIProxy` may be computed only if:

- it has a distinct feature name and schema;
- feed interval, gap and snapshot provenance are recorded;
- it is trained/validated separately from true event OFI;
- documentation and downstream code never label it as event-level OFI;
- its horizons do not imply unsupported sub-snapshot precision.

Switching feed fidelity requires a new feature/model version and validation; it is not a transparent substitution.

## Multi-Level OFI — QF-033

```text
MLOFI_W = sum_{k=1..K} w_k OFI_{k,W}
```

The aggregation structure is locked; levels, windows, weights and optional normalization are calibrated/learned. Start with a simple documented baseline. MLOFI may feed future-depth, impact, adverse-selection and cross-market models only after incremental OOS lift.

## Signed trade flow

Signed executed flow is a separate feature family. It does not replace OFI because it omits visible additions and cancellations. Side inference/semantics, aggregation window and source must be explicit. Trades between snapshots can improve a coarse public-L2 model but cannot reconstruct hidden order lifecycle.

## Microprice — QF-034 and QF-035

```text
MicroPrice = (Ask * Q_bid + Bid * Q_ask) / (Q_bid + Q_ask)
MicroDislocation = (MicroPrice - Mid) / Mid
MicroDislocation_bps = 10^4 * MicroDislocation
```

For valid non-crossed BBO and non-negative queues, MicroPrice lies within bid/ask. Zero queue sum or invalid/non-positive `Mid` invalidates the relevant result. Microprice is a short-horizon pressure/toxicity feature, not a fundamental fair value.

## Volatility and jumps

Volatility and jump measures condition survival, cancellation, adverse selection, response, recovery and sizing. They are not primarily directional predictors. Windows and thresholds are calibrated, computed from information available at decision time, and assessed for stability by regime. A jump label or future-known regime must not leak into current features.

## Feed fidelity and freshness

`PUBLIC_L2` may support snapshots, trades, coarse depth changes, opportunity survival and coarse response at compatible horizons. Exact add/cancel sequencing, queue movement, cancellation position and fine reaction time require event-level data not guaranteed by public snapshots. `NODE_EVENT/L4` is future/external-dependent and separately versioned.

Prediction validity requires feature freshness and coherent clocks. The model must expose unsupported fidelity rather than manufacture millisecond precision from coarse data.

## Tests and validation

- hand-computed QI, QI_K, bid/ask OFI and MLOFI sequences;
- equal-price equality branches and level changes;
- denominator, crossed-book, gap/reorder and reset cases;
- snapshot-proxy versus event-OFI schema separation;
- Python/Rust numerical parity within declared tolerance;
- temporal no-lookahead and feature as-of audits;
- ablation and EconomicLift/ModelValue after inference latency;
- drift and OOD by market, regime, size and feed mode.

## Sources

SRC-004 QF-028..035; SRC-002 architecture; SRC-005 Data/Risk; SRC-006 validation; SRC-007 sections 15–19 and quant microstructure; SRC-008 response features.
