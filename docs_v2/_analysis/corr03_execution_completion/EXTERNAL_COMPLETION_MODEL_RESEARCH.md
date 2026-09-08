# CORR-03 — External Completion Model Research

DOCUMENTATION STATUS: IMPLEMENTATION OPTIONS ONLY

| Topic | Primary/official reference | Retained lesson | Project disposition |
|---|---|---|---|
| probability calibration | [scikit-learn probability calibration](https://scikit-learn.org/stable/modules/calibration.html) | reliability diagrams compare predicted probability with observed frequency; Brier/LogLoss mix calibration and other predictive properties | use curves plus QF-095/096 and support, never one score alone |
| temporal validation | [scikit-learn TimeSeriesSplit](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.TimeSeriesSplit.html) | ordinary cross-validation can train on future and evaluate on past | chronological/walk-forward OOS is mandatory; exact splitter is not prescribed |
| log loss | [scikit-learn log_loss](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.log_loss.html) | binary log loss consumes aligned labels and probabilities; numerical clipping is explicit | Formula Book QF-096 remains authority; external library epsilon is not imported |
| sparse-bin shrinkage candidate | [Stan beta-binomial distribution](https://mc-stan.org/docs/functions-reference/beta-binomial-distribution.html) | beta-binomial is a transparent over-dispersed/smoothing family | candidate only; prior, pooling hierarchy and support thresholds remain `CALIBRATED` |

External material does not modify QF-095/096 or create a new Formula ID. Censoring treatment remains defined by project outcome semantics: unresolved attempts are retained and disclosed; binary fitting uses only authoritatively resolved labels. Maker time-to-event work is separate from the initial TT/TTT binary baseline.
