# 07 — Release Channels, Capabilities and Promotion

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Channels

`DEVELOPMENT` supports engineering/research and is non-Live by default. `CANDIDATE` supports controlled internal/canary validation. `STABLE` is the supported client release after promotion evidence. Stable means release maturity, not automatic Live permission.

```text
CODE -> UNIT -> INTEGRATION -> GOLDEN REPLAY -> BENCHMARK
     -> SHADOW -> MICRO-LIVE -> CANDIDATE -> CANARY -> STABLE
```

The same digest/core progresses. A rebuild creates a new candidate identity and cannot inherit evidence silently. Emergency promotion may shorten observation but retains unit, integration, golden replay and Shadow evidence.

## Capability algebra

```text
EffectiveCapability = CompiledSupport
                    ∩ ConfiguredEnablement
                    ∩ LicenseEntitlement
                    ∩ ReleaseChannelPolicy
                    ∩ ValidatedCapability
                    ∩ CurrentReadiness
                    ∩ RiskPermission
```

Each operand can only narrow the set. License does not imply validated; enabled does not imply validated; compiled does not imply validated. Live authorization is scoped by mode, market/route, size/capital, infrastructure, model/formula/schema versions and evidence support.

## Independent artifacts

Software updates, configuration changes and model promotions have distinct identities, validation and rollback. A model artifact binds model version/hash, feature schema, training/support metadata, evidence and fallback. A config change produces a new `config_hash`. Any material change invalidates dependent evidence according to PASS10 policy.

## Demotion

Breaking exchange changes, vulnerabilities, drift, incompatibility or field incidents may demote a channel/capability or set no-new-risk. Demotion preserves cancel, reconciliation, Recovery and data access. Promotion/demotion is audited and never inferred solely from artifact availability.
