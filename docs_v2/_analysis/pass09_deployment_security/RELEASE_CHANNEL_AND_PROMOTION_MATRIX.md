# Release Channel and Promotion Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Channel | Audience | Evidence floor | New-risk posture |
|---|---|---|---|
| `DEVELOPMENT` | Engineering/research | Build, unit checks and explicit experimental provenance | Replay/test only by default |
| `CANDIDATE` | Internal/canary installations | Integration, golden replay, benchmark, Shadow and Micro-live evidence applicable to capability | Only explicitly validated canary scope |
| `STABLE` | Supported client installations | Candidate/canary success, compatibility and rollback evidence, accepted vulnerabilities only | Still requires local capability/license/readiness/Risk |

## Promotion flow

```text
CODE -> UNIT -> INTEGRATION -> GOLDEN REPLAY -> BENCHMARK
     -> SHADOW -> MICRO-LIVE -> CANDIDATE -> CANARY -> STABLE
```

An emergency release may compress timing but not omit the minimum unit, integration, golden-replay and Shadow evidence. It is never an untested binary pushed directly to clients.

## Capability intersection

| Axis | Meaning | Cannot substitute for |
|---|---|---|
| Artifact compiled support | Code path exists | Validation or permission |
| RunMode/config | Operator requests a mode | License or evidence |
| License entitlement | Commercial feature allowed | Technical safety |
| Release channel | Artifact maturity cohort | Per-capability validation |
| `CapabilityManifest` | Evidence-backed scope, size and mode | Current readiness/Risk |
| Runtime Risk decision | Current action permitted | Missing artifact or capability |

Software, configuration and model promotion are separate release streams. A model change carries its own hash, model/feature-schema versions, support domain, validation evidence and fallback.
