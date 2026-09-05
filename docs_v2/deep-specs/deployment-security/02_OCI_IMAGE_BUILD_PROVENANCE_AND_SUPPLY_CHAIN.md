# 02 — OCI Image, Build Provenance and Supply Chain

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Artifact contract

The release is a provider-neutral OCI image, initially supported with Docker Engine/Compose on `linux/amd64`. A multi-stage build produces a minimal runtime without compiler, Cargo tooling or repository source. The root artifact is immutable; client material is mounted at runtime.

```text
Git revision + Cargo.lock + toolchain + build config
  -> builder
  -> OCI manifest/platform/digest
  -> SBOM + scan + signature/provenance
  -> private registry
  -> client download
  -> local verification
  -> non-ready activation
```

## Identity

Semantic version and channel are labels; the OCI digest is the byte identity. Release metadata records Git revision, dependency lock, builder/toolchain, build timestamp, platform, schema ranges, SBOM, scan and signer identity. Production selects a version/digest pair and never follows `latest`.

## Promotion controls

1. Produce the candidate from declared immutable inputs.
2. Inspect platform and minimal-runtime contents.
3. Generate an SBOM bound to the digest.
4. Scan dependencies/base/artifact; document any accepted finding.
5. Sign/attest the digest under release policy.
6. Publish immutably to a private registry.
7. Give clients pull-only credentials.
8. Verify digest, signature, channel and compatibility locally before owner change.

A critical known vulnerability with no explicit assessment/acceptance blocks promotion. Compromise or signature failure revokes the candidate and triggers release-security response; it does not force-stop a currently verified safe owner without a separate risk assessment.

## Open tooling

Base image, static/dynamic linkage, registry, SBOM format/generator, scanner, signing scheme/key storage and reproducible-build target remain `OPEN`. Tool choice must preserve offline/local verification, key separation, auditability and rollback to a known digest.
