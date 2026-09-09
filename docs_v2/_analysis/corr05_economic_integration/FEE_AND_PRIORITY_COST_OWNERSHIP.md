# Fee and Priority-Cost Ownership

Exchange/trading fees are applied through QF-016 in each executed scenario path exactly once, including debit-asset and rebate semantics. Infrastructure recurring cost belongs to the infrastructure/accounting bucket, not order fees.

CORR-04 found no verified current V1 user-controlled numeric paid per-order priority mechanism. Status remains `FUTURE / EXTERNAL_REVALIDATION`; current priority cost is zero because applicability is not established, not because future service would be free.

If such a mechanism is later authoritatively verified, its actual action-level charge belongs once in the affected execution scenario cashflow. Requested level, actual charge and observed benefit remain separate. The benefit must be learned through changed latency/sequencing/outcome distributions; payment never guarantees capture. Activation requires explicit scope, bounded policy, Risk compatibility and human review.
