# Disaster Recovery: Data vs Authority

Backed-up config/state/journal/checkpoints restore evidence, not trading permission. Signer recovery/revocation is a separate client-controlled procedure. A signer without reconciled state cannot become READY; restored state without valid fenced signer cannot trade. Suspected host/signer compromise requires no-new-risk, revocation/rotation, exchange truth and cold non-ready restart. Vendor never becomes custodian.
