# Maker Fill Target Contract

| Target | Meaning | Unit | Censoring | Consumer |
|---|---|---|---|---|
| AnyFillByH | at least one positive fill by H | probability | yes | exposure/queue analysis |
| FirstFillTime | time to first positive fill | time | right-censored | maker timing |
| FullFillByH | requested quantity complete by H | probability | yes | route completion input |
| FullFillTime | time to requested fill | time | right-censored | completion timing |
| FilledQuantityByH | actual cumulative q by H | asset quantity | observed/censored | continuation/Recovery distribution |
| PartialFillProbability | positive but incomplete by H | probability | explicit | exposure distribution |

SRC-004 calls QF-051–053 only “time-to-fill”; first-versus-full target is OPEN and must be typed before use.
