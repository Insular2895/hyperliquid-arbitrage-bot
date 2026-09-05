# 05 — Hysteresis, Cooldown and Relocation Governance

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Purpose

Relocation and asset-class changes operate on slower, evidence-accumulating horizons than opportunity execution. Hysteresis prevents capital from chasing alternating rankings; cooldown limits reaction frequency; persistence requires an advantage to survive long enough to matter.

## Locked structure and calibrated values

The existence of a positive relocation advantage, hysteresis/cooldown and Risk approval is locked by the closure sources. The exact `RelocationThreshold`, cooldown, persistence duration, evidence windows, class transition bounds and override/escalation values are calibrated.

No move is authorized solely because one current tick makes a destination rank first. Evidence may include point-in-time recent/medium/long Atlas utility, validated capacity, opportunity frequency/survival, competition, exitability, inventory and model confidence. FAST signals can nominate; slower evidence authorizes.

## Governance state

Each candidate records destination/path, first/last qualifying time, value series, evidence versions, current cooldown, last move, current class and reason. Material policy changes are versioned in config/RunManifest. Missing or OOD evidence reduces activity.

## Reversibility

Relocation and classification can be promoted or demoted. Capacity or utility deterioration may shrink or reverse placement after governance conditions pass; it never waits for an assumption of monotonic growth. Safety/Recovery can preempt cooldown because they are not ordinary optimization moves.

## Calibration and failure tests

Replay alternating destination attractiveness and compare total move cost, missed opportunity and time trapped in an inferior state. Shadow evaluates move/stay counterfactuals without capital effects. Micro-live validates actual cost/latency at bounded size. Failure conditions include excessive flip-flop, stale evidence, unsupported class change, cooldown bypass, no audit reason or material move without Risk eligibility.

Sources: SRC-001 hysteresis/capital horizons; SRC-002 Capital Relocation discussion; SRC-003 Bridge policy experiments; SRC-004 QF-072; SRC-005 §74; SRC-006 hysteresis test.
