# QF-044–QF-055 — Survival, Capture, Maker Fill and Adverse Selection

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| QF | Expression | Symbols / output unit | Preconditions | Failure semantics | Golden requirements |
|---|---|---|---|---|---|
| QF-044 | `S(t∣X)=P(T>t∣X)` | probability | defined edge-death event, horizon/features, valid model | unsupported/OOD/missing artifact → unavailable/low confidence | monotone/range/endpoints and censoring |
| QF-045 | `h_k=P(T∈[t_k,t_{k+1})∣T≥t_k,X)`; baseline `σ(β_k^TX)` | probability per bin | at-risk observation, ordered bins, learned β | invalid probability/artifact/support → invalid | logits, range, at-risk/censored cases |
| QF-046 | `S_k=Π_{j=1}^k(1-h_j)` | probability | every h_j∈[0,1], exact source index 1..k | missing/invalid hazard invalidates suffix | k=1, multi-bin, h=0/1; guards against legacy j<k |
| QF-047 | `t_50=inf{t:S(t)≤0.5}` | time | valid survival curve/horizon | no crossing → censored `>model_horizon`; never fabricated endpoint | crossing/interpolation policy, equality, no crossing |
| QF-048 | `E_L[S(L)]`; discrete `Σ_mP(L∈B_m)S(ℓ_m)` | probability | aligned time units/origin; valid normalized latency distribution and survival | missing bins/mass/model invalid | deterministic L, normalized bins, extreme survival |
| QF-049 | `E[Edge_{t+L}∣X_t]` | edge ratio/bps as declared | point-in-time features, latency and learned edge distribution | OOD/stale/missing model unavailable | distribution mean and no exponential shortcut |
| QF-050 | `P(Edge_{t+L}>E_minimum∣X_t)` | probability | same edge unit/definition; calibrated threshold; valid learned distribution | threshold/unit/model mismatch invalid | strict threshold equality, 0/1/interior probabilities |
| QF-051 | `S_f(t∣X)=P(T_f>t∣X)` | probability | maker order context, fill event, horizon/features/model | cancellation/censoring/missing model handled explicitly | range/monotonicity/censor cases |
| QF-052 | `F_f(t∣X)=1-S_f(t∣X)` | probability | exact same QF-051 event/horizon/artifact | mismatch/invalid survival invalid | complement equality at multiple times |
| QF-053 | `E[T_f]=∫_0^∞S_f(t)dt` plus discrete survival sum | time | valid survival and integration/support convention | truncated/conditional value must be labelled; divergent/unknown tail invalid | analytic distribution, discrete approximation, censored horizon |
| QF-054 | `(P_f-Mid_{t_f+h})/P_f` | ratio, positive adverse | filled BUY; P_f>0; explicit future-mid horizon | missing fill/reference or invalid price → invalid | adverse/favorable/flat and horizon identity |
| QF-055 | `(Mid_{t_f+h}-P_f)/P_f` | ratio, positive adverse | filled SELL; P_f>0; explicit future-mid horizon | missing fill/reference or invalid price → invalid | adverse/favorable/flat and side symmetry |

Survival and maker-fill quantities are distinct event processes. QF-049 is a learned conditional expectation; the source imposes no exponential edge-decay law. All predicted outcomes retain artifact, feature, horizon, point-in-time and support/OOD provenance.
