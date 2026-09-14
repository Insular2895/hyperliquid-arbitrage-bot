# Fee Asset and Route Value Audit

| Case | Terminal output affected? | Economic value affected? | Canonical treatment |
|---|---:|---:|---|
| fee in B | yes | yes | QF-016 output and delta, counted once |
| fee in A | not necessarily | yes | QF-016 asset delta plus explicit valuation |
| fee in C | no direct B reduction | yes | QF-016 asset delta plus explicit valuation |
| rebate in B | yes | yes | QF-016 output and delta, counted once |
| rebate in C | no direct B increase | yes | QF-016 asset delta plus explicit valuation |

QF-019/QF-020 compare terminal B. Total economic ranking also consumes all side deltas under one declared point-in-time numeraire/version; absent valuation evidence is invalid, not zero.
