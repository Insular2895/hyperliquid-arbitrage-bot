# Priority Economic Hook Contract

`STATUS: CURRENT MECHANISMS VERIFIED 2026-09-09 — CAPABILITY/EVIDENCE-GATED`

This remains a provenance/evidence contract, not a Formula, autonomous optimizer, Risk gate or activation decision.

```text
PriorityEvidence {
  PriorityPolicyId
  scope: GOSSIP_READ | IOC_WRITE | ALO_WRITE
  verified_venue_product_action_scope
  eligibility_and_grouping
  requested_slot_or_rate
  charge_basis: AUCTION | FILLED_NOTIONAL | RESTING_NOTIONAL
  actual_charged_amount?
  charged_asset_and_source_balance?
  charge_time?
  observed_sequencing_ack_fill_evidence?
  source_retrieval_and_revalidation_id
  evidence_class
}
```

`GOSSIP_READ` auction cost is owned once by the corresponding feed/infrastructure experiment. `IOC_WRITE` and `ALO_WRITE` charges belong once in the affected execution scenario cashflow; IOC zero-fill has zero priority charge under the documented filled-notional basis, while ALO is charged on resting notional at placement regardless of later fill. Benefit is represented only through the changed validated outcome distribution. No priority payment bypasses Risk, price protection, sizing or Reservations.
