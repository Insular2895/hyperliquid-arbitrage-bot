# 02 — Edge Survival, Hazard and Capture

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

## Economic lifetime

For route `r`, size `q` and observation time `t`, the edge must be the authoritative net executable edge, not a theoretical price spread. Birth requires the applicable entry condition plus valid/fresh books, executable size and authoritative cost/risk prerequisites. Death occurs when the opportunity no longer clears the applicable execution threshold, validated capacity falls below `q`, or another authoritative execution condition makes it non-viable.

PASS 02 does not define `E_minimum`, fees, slippage, sizing or Risk gates. It consumes them. Entry/exit hysteresis may be calibrated with `E_enter > E_exit` to avoid label flicker.

## Episode and censoring contract

An `OpportunityEpisode` must support route/size, birth/death timestamps, edge path, initial/max edge, book state at birth, first correction, dominant decay leg where observable, death reason, regime and censor state. Near opportunities, rejected opportunities and normal states are also recorded to limit selection bias.

If recording ends, a feed disconnects or eligibility is removed while the edge remains alive, the episode is `RIGHT_CENSORED`; recording end is not fabricated as death. Feature construction and labels use point-in-time clocks consistent with Replay.

## Canonical survival objects

With remaining lifetime `T` and current state `X`:

```text
S(t|X) = P(T > t | X)                                      QF-044
h_k(X) = P(T in [t_k,t_{k+1}) | T >= t_k, X)              QF-045
S_k = product_{j=1..k}(1-h_j)                              QF-046
t50 = inf{t : S(t) <= 0.5}                                 QF-047
```

The mathematical object and survival-from-hazard relation are locked. Hazard coefficients and estimator are learned. `S` must remain within `[0,1]`, be non-increasing over its supported horizon, and expose horizon support. If 0.5 is not crossed, return `t50 > model_horizon`.

The discrete-hazard baseline may use `h_k(X)=sigma(beta_k^T X)` with learned coefficients. Continuous-time notation can explain hazard, but the canonical production formula is the Formula Book discrete form.

## Cause-specific hazard

Potential causes include aggressive trade consumption, cancellation, repricing, cross-market movement and other. Cause decomposition is not an initial production dependency. Overall edge-death hazard is more directly observable. Cause-specific estimates require sufficient event fidelity and validated labels; public snapshots may only support coarse attribution.

## Capture and latency

For measured end-to-end latency distribution `L`:

```text
P_capture = E_L[S(L)]                                      QF-048
P_capture,s = E_{L_s}[S(L_s)]                              QF-085
```

The empirical histogram estimator uses latency mass in each bucket and survival at a declared representative. `S(E[L])` is not interchangeable with `E[S(L)]`; nonlinearity and tail latency make the former biased for capture.

The latency distribution must correspond to the same decision path, infrastructure profile, market/feed context and time semantics being evaluated. Unsupported latency or survival horizons lower confidence or invalidate the estimate.

## Arrival-edge distribution

Survival alone loses information about partial decay and negative tails. The model also produces:

```text
E_arrival = E[Edge_{t+L} | X_t]                            QF-049
P_exec = P(Edge_{t+L} > E_minimum | X_t)                  QF-050
Correction(h) = (E_0 - E_h) / E_0                         QF-082
```

QF-049/050 are learned distributions/outputs, not exponential-decay assumptions. QF-082 equals one when the edge disappears and can exceed one when the edge crosses zero. Handle `E_0=0` as invalid for the normalized correction measure.

## Inputs

Supported inputs can include current edge/age/derivative, route class, size/capacity, leg spread/depth/slope/levels, QI/MLOFI, event OFI or labelled proxy, signed flow/intensity, cancellation/replenishment, microprice, volatility/jumps, regime, activity, time of day, opportunity density and cross-market state. Every feature requires as-of time, definition/version, provenance, freshness and validity.

## Outputs

The participant-facing survival forecast logically contains:

- survival probabilities at supported horizons;
- hazard probabilities or rate representation as applicable;
- `p_survive_arrival` / `p_capture`;
- `p_above_threshold_arrival`;
- expected arrival edge and quantiles;
- `edge_half_life` or a bounded-horizon statement;
- optional dominant decay leg;
- confidence/OOD and model/feature provenance.

The authoritative `EdgeSurvivalForecast` schema remains owned by the Data Contracts pass.

## Consumers and prohibitions

- Execution/Strategy: forecast input, never independent authorization.
- Risk: direct probability, tails and confidence gates.
- Sizing/Slicing: capacity, survival and decay trade-offs.
- Infrastructure: economic value of measured latency distributions.
- Simulator: scenario distribution input.
- Market Atlas: windowed survival/correction statistics.

Do not use `current_edge × P_survive` as full route EV. Edge death during execution may produce partial fills, inventory and recovery loss; the Simulator owns the outcome distribution.

## Calibration and failure modes

Start with empirical survival stratified by route, edge, liquidity, volatility and size/depth where support exists. Compare to naive constant survival, then challenge with discrete hazard and later models. Use temporal split, walk-forward, right-censor-aware estimation, calibration curves, QF-094 observed survival, Brier/Log Loss, regime/asset slices and replay/micro-live predicted-versus-realized checks.

Failures include label contamination, lookahead, censor mishandling, regime/feature drift, OOD size, stale inputs, tail extrapolation, invalid/nonmonotone probabilities and latency-support mismatch. Safe behaviour is conservative empirical fallback, reduced capability or rejection.

## Sources

SRC-004 QF-044..050, 082, 083, 085 and 094..096; SRC-005 Risk/Data contracts; SRC-006 validation; SRC-007 participant and quant sections; SRC-008 infrastructure/simulator interfaces.
