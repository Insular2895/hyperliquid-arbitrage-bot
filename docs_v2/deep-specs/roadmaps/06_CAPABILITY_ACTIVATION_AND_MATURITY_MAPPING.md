# Capability Activation and Maturity Mapping

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Independent axes

The system must not collapse these axes:

1. code/type support;
2. configured RunMode/feature enablement;
3. release channel and license scope;
4. M0–M5 validation maturity;
5. current readiness/health;
6. current RiskDecision;
7. market/mode/size/model/infra/version support.

Effective permission is their intersection. A true value on one axis cannot widen another.

## Maturity semantics

| Level | Evidence meaning | Capital meaning |
|---|---|---|
| M0 SPECIFIED | Purpose/contracts/invariants/tests defined | None |
| M1 UNIT VALIDATED | Unit/golden/property correctness | None |
| M2 REPLAY VALIDATED | Reproducible historical/failure behavior | None |
| M3 SHADOW VALIDATED | Stable same-Core real-time no-effect behavior | None |
| M4 MICRO-LIVE VALIDATED | Bounded real intervention calibrated | Probe/validated bounded scope |
| M5 LIVE VALIDATED | Sustained exact-scope evidence | Scaled validated, reversible |

A capability cannot exceed its least-mature critical dependency. Pure technical utilities may not need capital-bearing levels; order/Risk/fill/capital capabilities cannot skip required Replay, Shadow or Micro-live.

## CapabilityManifest as bridge

```text
implementation
→ phase DoD
→ stage evidence
→ validation decision
→ CapabilityManifest scope
→ configured/ready/licensed intersection
→ per-action RiskDecision
→ possible capital effect
```

The manifest scope includes strategy, markets/routes, mode, size range, model/artifact versions, validation level, restrictions and relevant build/config/formula/schema/infra identity. Missing exact coverage fails closed.

## Divergent maturity example

Recorder may be M5 operationally; public-feed Book M5 for supported markets; TT OWA M4; TTT Shadow/M3; a Participant Challenger M2; MT disabled; Bridge M1/M2. This is a healthy state. “The bot is M5” is invalid shorthand.

## Activation and demotion

The canonical sequence is recorded in [CAPABILITY_ACTIVATION_SEQUENCE.md](../../_analysis/pass12_build_validate_scale/CAPABILITY_ACTIVATION_SEQUENCE.md). Every capability can `PROMOTE`, `HOLD`, `SHRINK`, `FALLBACK`, `SUSPEND`, `DEMOTE` or `DISABLE` as its domain permits. M5 never means permanent.
