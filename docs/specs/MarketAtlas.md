# MarketAtlas

## Purpose

Résumer la structure économique historique et piloter HOT/WARM/COLD.
## Responsibilities

Scores/connectivity/exit quality/opportunity density, classifications et policy artifacts.
## Non-responsibilities

Ne modifie pas automatiquement les paramètres stratégiques live.
## Inputs

Derived markets/routes/opportunities/inventory outcomes.
## Outputs

Versioned AtlasSnapshot et activation recommendations.
## Dependencies

Recorder, ReplayEngine, GlobalGraph, CapitalReachabilityEngine.
## State

Rolling/long-term summaries, champion policy version.
## Algorithms / formulas

QF economics agrégées; policy explicitly specified, no opaque universal score.
## Invariants

CORE/TRANSIT/EXCLUDED and HOT states distinct; historical fidelity unaffected.
## Failure modes

Selection bias, regime overfit, thrash, stale atlas.
## Risk interactions

Classification may restrict risk; cannot relax hard gates.
## Performance requirements

Heavy build offline; live lookup bounded.
## Metrics

Coverage, stability, promotions, missed/costly compute, lift.
## Persistence

Atlas manifest/dataset/config and change history.
## Configuration

Windows, hysteresis, eligibility and review policy.
## Tests

Walk-forward, policy A/B replay, churn, sparse regimes.
## Maturity requirement

M2 policy; M3 shadow; M4 activation per capability.
## Open calibrated parameters

Scores, windows, HOT/WARM/COLD thresholds/hysteresis.
