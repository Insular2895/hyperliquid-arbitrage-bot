# External Formula Rule Register

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

No Internet or external revalidation was performed during PASS11. These are dependencies to verify before implementation/Live use.

| Rule ID | QFs | External fact | Required evidence | Failure behavior | Status |
|---|---|---|---|---|---|
| EXF-001 | 007 | current size quantum / `szDecimals` and any lot/minimum rule | official exchange docs/API metadata, effective time, fixture | disable affected market/new risk | EXTERNAL_RULE_REQUIRES_REVALIDATION |
| EXF-002 | 008 | spot price significant figures, decimal places, integer-price behavior | official docs + accepted/rejected API fixtures | PriceQuantizer unknown/reject | EXTERNAL_RULE_REQUIRES_REVALIDATION |
| EXF-003 | 009–010,016 | minimum size/notional, protection and partial acceptance semantics | official order rules/API responses | full-fill/minimum gate rejects | EXTERNAL_RULE_REQUIRES_REVALIDATION |
| EXF-004 | 014 | current fee endpoint/fields, account tiers, maker/taker and rebates | official API/docs + account fixture | FeeEngine unknown/reject | EXTERNAL_RULE_REQUIRES_REVALIDATION |
| EXF-005 | 015–016 | actual fee debit asset and fill/account delta semantics | official API payloads/account reconciliation | unknown asset delta blocks conversion/accounting | EXTERNAL_RULE_REQUIRES_REVALIDATION |
| EXF-006 | 016,068,070,075 | market metadata changes and point-in-time application | official metadata stream/snapshot contract | version mismatch invalidates path/size | EXTERNAL_RULE_REQUIRES_REVALIDATION |

External evidence never edits a historical result in place. It creates effective-dated Metadata/Fee/Formula compatibility, fixtures and revalidation scope.
