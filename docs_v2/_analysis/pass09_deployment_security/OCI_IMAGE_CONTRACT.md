# OCI Image Contract

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Artifact identity

| Element | Contract |
|---|---|
| Format | Provider-agnostic OCI image; Docker Engine + Compose is the initial supported runtime |
| Architecture | `linux/amd64` V1; other architectures require explicit build and validation |
| Build | Multi-stage; runtime excludes compiler, Cargo tooling and source tree |
| Runtime contents | Minimal executable, required CA/time-zone/runtime assets, metadata and stable bundled models only |
| Version | Semantic version plus Git revision, build timestamp and schema compatibility metadata |
| Identity | Immutable digest is authoritative; tags are human navigation only |
| Pinning | Production activation pins an explicit version and digest; no production `latest` |
| Provenance | Git revision, dependency lock, toolchain and build configuration retained |
| Registry | Private OCI registry direction; client credential read-only |
| Integrity | Digest and signature verified before activation; SBOM and vulnerability scan attached |

## Promotion invariants

The same core artifact progresses through Replay, Shadow, Micro-live, Candidate/canary and Stable. Run mode and licensed capability are configuration/entitlement axes; a separate Live binary is not the baseline. Compiled, enabled, licensed and validated are distinct states.

## Runtime boundary

The image is replaceable and must not contain client secrets or mutable economic truth. Persistent state is mounted explicitly. Stable models may ship in an image; independently updated models require their own signed/hash-addressed manifest, model version and feature-schema compatibility.

## Open implementation choices

Exact base image, static-versus-dynamic linkage, registry provider, signing technology and scan tooling remain implementation choices. They must satisfy the locked behavior and PASS10 evidence gates before production use.
