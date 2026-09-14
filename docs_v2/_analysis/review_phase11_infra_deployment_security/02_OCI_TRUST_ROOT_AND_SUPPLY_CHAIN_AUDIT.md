# OCI Trust Root and Supply Chain Audit

Source revision/lock/toolchain → digest/SBOM/scan → signature/provenance → immutable registry → local verification. Verification is performed by a previously trusted component anchored outside the candidate. Digest/signature/signer/provenance mismatch blocks candidate only. Root rotation is versioned. Cosign/Notary/Sigstore/GPG/HSM choices remain OPEN.
