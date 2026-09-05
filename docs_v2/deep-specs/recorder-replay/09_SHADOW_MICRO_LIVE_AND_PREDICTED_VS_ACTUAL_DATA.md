# Shadow, Micro-live and Predicted-versus-actual Data

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

Shadow uses real market/account observation and the production Core with `NullShadowTransport`. It records Opportunities, FeatureSnapshots, forecasts, RiskDecisions, ExecutionPlans, would-submit intents, latency and subsequent market outcomes. `ActualAccountState` and `ShadowCounterfactualState` are separate and never reconciled into one truth.

MicroLive uses real market, real execution and real account under small validated risk caps. For every order/execution it pairs predicted and actual fill quantity/time, slippage, latency stages, fees, PnL and Recovery. Size/market/regime/model support is recorded so calibration does not pool incompatible observations.

Champion output may affect decisions; Challenger output is recorded but never enters RiskDecision before a versioned promotion. Prediction records identify model version and input snapshot, then attach realized outcome/error when known.

The comparison dataset is append-only evidence. Research creates new model artifacts and validation reports; production does not silently self-train or promote. Simulation underestimation, drift, OOD or unexplained tail outcomes feed Risk/Validation downgrade paths.

Acceptance demonstrates stable Shadow, complete would-action capture, bounded MicroLive exposure, prediction/outcome join completeness and zero contamination between actual and counterfactual balances.
