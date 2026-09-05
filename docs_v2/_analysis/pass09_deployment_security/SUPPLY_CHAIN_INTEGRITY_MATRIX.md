# Supply-Chain Integrity Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

| Stage | Locked requirement | Evidence / rejection | Tooling status |
|---|---|---|---|
| Source revision | Every artifact maps to an immutable Git revision | Clean revision recorded in provenance | CI/VCS implementation OPEN |
| Dependency lock | Resolved dependency graph is pinned | `Cargo.lock` hash and dependency inventory | Scanner choice OPEN |
| Toolchain/build | Toolchain and build configuration recorded; reproducible direction | Builder identity and build attestation | Reproducibility level OPEN |
| Artifact | Minimal multi-stage OCI runtime image | OCI manifest/platform inspection | Base image choice OPEN |
| SBOM | Machine-readable component inventory accompanies release | SBOM bound to digest | Format/generator OPEN |
| Vulnerability scan | Known findings assessed; no unaccepted critical finding promoted | Signed/retained scan report and acceptance | Scanner/SLAs OPEN |
| Signature | Release authenticity verified before activation | Signature bound to immutable digest | Signing scheme/KMS OPEN |
| Digest | Expected digest pins the exact bytes | Wrong digest rejected | OCI digest locked |
| Registry | Private distribution; client pull scope read-only | Registry audit and credential-scope test | Provider OPEN |
| Download | Candidate staged without changing active owner | Download log and size/digest metadata | Client implementation OPEN |
| Verification | Digest, signature, channel and compatibility checked locally | Fail closed before stop/replace | Verification library OPEN |
| Activation | Only verified compatible artifact enters startup; it begins non-ready | DeploymentManifest and update state trace | Orchestration implementation OPEN |
| Audit | Release/promotion/update/rollback evidence retained | Tamper-evident release record | Retention/backend OPEN |

Release identity includes semantic version, Git revision, image digest, build timestamp and relevant schema versions. Tags are mutable navigation aids, not trust anchors. Production does not track `latest`.
