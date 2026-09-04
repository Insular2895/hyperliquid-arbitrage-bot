# Config, Parameter Governance and Client Bounds

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Constitutional versus tunable

Constitutional rules include no blind retry, exchange truth/actual fill precedence, no new risk on stale/invalid or unreconciled state, reservation before orders, hard inventory enforcement, reconciliation before readiness, no martingale and bounded recovery. Configuration cannot disable or weaken them.

Tunables include freshness, spread/impact/participation/volatility/jump, probability/confidence/OOD/disagreement, tail/loss, inventory, maker age/exposure, recovery, drawdown, quality, infrastructure and sizing/scaling bounds. Their policy structure is constitutional; exact values are evidence-derived.

## Required parameter record

Every important parameter carries name, unit, scope, owner, value and valid range, provenance class, config version, effective timestamp, evidence IDs, update/rollback process, hot-reload permission and whether an ExecutionPlan pins it. Provenance is one of `CALIBRATED`, `LEARNED`, `EXCHANGE_RULE`, `SAFETY_DEFAULT`, `USER_TIGHTENABLE`, or explicit `OPEN`; hard rules are `CONSTITUTIONAL`.

No magic number may exist only in code. Unknown or invalid values use conservative safety defaults where source-supported, otherwise block affected readiness.

## Validation and change

Startup rejects inconsistent bounds, negative limits, probabilities outside `[0,1]`, unsupported metadata or disabled hard checks. Production changes are authenticated, atomic, versioned, logged and rollback-capable. Existing ExecutionPlans retain their pinned version across legs; emergency hard stops may interrupt.

No normal risk-config switch occurs during a critical transition. A new policy cannot retroactively redefine real exposure as safe. Replay compares policy versions on identical data before promotion.

## Client/operator boundary

A client may tighten a validated limit, such as using 100 when the validated maximum is 500. Profiles are presets within the same constitutional floor, not permission tiers. Clients/operators may lower limits and set kills; they cannot ignore stale state, UNKNOWN orders, reconciliation, precision, reservations or hard inventory.

Unsupported configurations do not silently coerce into aggressive operation: they are rejected or prevent `READY`. There is no dangerous super-admin bypass.

The exhaustive parameter-family inventory is [RISK_PARAMETER_GOVERNANCE](../../_analysis/pass05_risk/RISK_PARAMETER_GOVERNANCE.md). Source: SRC-005 lines 3137–3224 and 3945–4020.
