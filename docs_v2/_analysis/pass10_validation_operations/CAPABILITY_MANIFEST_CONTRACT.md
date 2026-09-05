# CapabilityManifest Contract

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Canonical validated capability

Source-backed mandatory fields are:

```text
ValidatedCapability {
  strategy
  market_scope
  size_range
  execution_mode
  model_versions
  validation_level
  valid_from
  last_review
  restrictions
}
```

A release carries a CapabilityManifest containing zero or more such entries and an immutable link to its validation evidence. Build, configuration, release channel, current readiness and Risk permissions remain independent intersections; they do not become new mandatory `ValidatedCapability` fields by invention.

Runtime permission is:

```text
CompiledSupport ∩ ConfiguredEnablement ∩ LicenseEntitlement
∩ ReleaseChannelPolicy ∩ ValidatedCapability
∩ CurrentReadiness ∩ RiskPermission
```

If no manifest entry covers the exact strategy/market/size/mode/model scope, the runtime refuses new risk with a machine-readable reason. It never rounds up to a broader size, substitutes a model silently or infers authority from available code. Safe cancel, reconciliation, Recovery and read-only diagnostics remain available according to Risk.

Optional evidence metadata—EvidenceId, report hash, expiry/review trigger, infrastructure/config/formula/schema identity—belongs in linked versioned evidence unless the Data owner later extends the schema.
