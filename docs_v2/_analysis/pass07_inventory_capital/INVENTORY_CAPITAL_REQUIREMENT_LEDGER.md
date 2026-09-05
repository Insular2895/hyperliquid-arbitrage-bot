# Inventory / Capital Requirement Ledger

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

This ledger classifies every one of the **545/545** unique PASS00 Inventory/Capital/Sizing domain-index rows. Original titles remain in `../domain_indexes/INVENTORY_CAPITAL_SIZING.md`; all 545 source ranges were reopened and returned content. PASS00 status remains visible as provenance; reviewed closure corrections determine the PASS07 disposition and are listed in `CONFLICT_RESOLUTION.md`.

## Coverage summary

| Classification | Count |
|---|---:|
| `INVENTORY-OWNED` | 27 |
| `CAPITAL-OWNED` | 23 |
| `BRIDGE-OWNED` | 16 |
| `SIZING-OWNED` | 11 |
| `PORTFOLIO-OWNED` | 5 |
| `ACCOUNTING-INTERFACE` | 36 |
| `CROSS-DOMAIN` | 427 |
| **TOTAL** | **545** |

| Disposition | Count |
|---|---:|
| `MASTER` | 24 |
| `DEEP_SPEC` | 246 |
| `CROSS_DOMAIN_PASS08` | 37 |
| `FORMULA_REFERENCE` | 39 |
| `OPEN_ITEM` | 1 |
| `SUPERSEDED` | 0 |
| `REJECTED` | 2 |
| `RESEARCH/FUTURE` | 196 |
| **TOTAL** | **545** |
| **Destinationless** | **0** |

`DEEP_SPEC` on a cross-domain row means PASS07 documents only the Inventory/Capital consumer boundary; its completed or future owning domain remains authoritative.

## Row-level disposition

| Requirement | Classification | PASS00 status | PASS07 disposition | Source locator | Destination |
|---|---|---|---|---|---|
| `REQ-QUANT-0001` | `CROSS-DOMAIN` | `LOCKED` | `CROSS_DOMAIN_PASS08` | SRC-001 lines 20–50 | PASS08 Market Graph/Routes/Atlas |
| `REQ-SEC-0001` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-001 lines 51–67 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0003` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-001 lines 233–256 | source provenance / owning domain research |
| `REQ-VALID-0002` | `CROSS-DOMAIN` | `FUTURE` | `RESEARCH/FUTURE` | SRC-001 lines 369–390 | source provenance / owning domain research |
| `REQ-EXEC-0006` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-001 lines 480–502 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RECOV-0002` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-001 lines 555–576 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RECON-0001` | `CROSS-DOMAIN` | `OPEN` | `DEEP_SPEC` | SRC-001 lines 577–611 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-CAP-0001` | `CAPITAL-OWNED` | `FUTURE` | `RESEARCH/FUTURE` | SRC-001 lines 725–763 | 08 master; deep 03–05/10 |
| `REQ-ACCT-0002` | `ACCOUNTING-INTERFACE` | `LOCKED` | `MASTER` | SRC-001 lines 764–786 | 08 master; deep 10 |
| `REQ-RISK-0007` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-001 lines 787–818 | source provenance / owning domain research |
| `REQ-GRAPH-0002` | `CROSS-DOMAIN` | `RESEARCH` | `CROSS_DOMAIN_PASS08` | SRC-001 lines 1047–1094 | PASS08 Market Graph/Routes/Atlas |
| `REQ-BRIDGE-0001` | `BRIDGE-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-001 lines 1138–1169 | 08 master; deep 04–05/09 |
| `REQ-HWC-0001` | `CROSS-DOMAIN` | `RESEARCH` | `CROSS_DOMAIN_PASS08` | SRC-001 lines 1232–1251 | PASS08 Market Graph/Routes/Atlas |
| `REQ-RESEARCH-0004` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-001 lines 1252–1275 | source provenance / owning domain research |
| `REQ-INFRA-0003` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-001 lines 1293–1304 | source provenance / owning domain research |
| `REQ-CAP-0002` | `CAPITAL-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-001 lines 1305–1361 | 08 master; deep 03–05/10 |
| `REQ-BRIDGE-0002` | `BRIDGE-OWNED` | `LOCKED` | `MASTER` | SRC-001 lines 1362–1399 | 08 master; deep 04–05/09 |
| `REQ-EXEC-0011` | `CROSS-DOMAIN` | `CALIBRATED` | `DEEP_SPEC` | SRC-001 lines 1435–1454 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-ACCT-0003` | `ACCOUNTING-INTERFACE` | `LOCKED` | `MASTER` | SRC-001 lines 1455–1476 | 08 master; deep 10 |
| `REQ-ACCT-0004` | `ACCOUNTING-INTERFACE` | `LOCKED` | `MASTER` | SRC-001 lines 1495–1520 | 08 master; deep 10 |
| `REQ-ACCT-0005` | `ACCOUNTING-INTERFACE` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-001 lines 1546–1550 | 08 master; deep 10 |
| `REQ-REPLAY-0003` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-001 lines 1600–1640 | source provenance / owning domain research |
| `REQ-VALID-0005` | `CROSS-DOMAIN` | `FUTURE` | `RESEARCH/FUTURE` | SRC-001 lines 1671–1692 | source provenance / owning domain research |
| `REQ-VALID-0006` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-001 lines 1693–1734 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0015` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-001 lines 1735–1769 | source provenance / owning domain research |
| `REQ-BRIDGE-0003` | `BRIDGE-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-001 lines 1895–1896 | 08 master; deep 04–05/09 |
| `REQ-EXEC-0017` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-001 lines 1929–2008 | source provenance / owning domain research |
| `REQ-INV-0001` | `INVENTORY-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-001 lines 2013–2014 | 08 master; deep 01–03 |
| `REQ-INFRA-0004` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-001 lines 2015–2027 | source provenance / owning domain research |
| `REQ-GRAPH-0006` | `CROSS-DOMAIN` | `REJECTED` | `CROSS_DOMAIN_PASS08` | SRC-001 lines 2028–2056 | PASS08 Market Graph/Routes/Atlas |
| `REQ-ACCT-0007` | `ACCOUNTING-INTERFACE` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-001 lines 2130–2140 | 08 master; deep 10 |
| `REQ-CAP-0003` | `CAPITAL-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-001 lines 2141–2151 | 08 master; deep 03–05/10 |
| `REQ-ACCT-0008` | `ACCOUNTING-INTERFACE` | `REJECTED` | `RESEARCH/FUTURE` | SRC-001 lines 2160–2204 | 08 master; deep 10 |
| `REQ-HWC-0007` | `CROSS-DOMAIN` | `RESEARCH` | `CROSS_DOMAIN_PASS08` | SRC-001 lines 2205–2268 | PASS08 Market Graph/Routes/Atlas |
| `REQ-CAP-0004` | `CAPITAL-OWNED` | `LOCKED` | `MASTER` | SRC-001 lines 2271–2291 | 08 master; deep 03–05/10 |
| `REQ-INFRA-0005` | `CROSS-DOMAIN` | `CALIBRATED` | `DEEP_SPEC` | SRC-001 lines 2292–2324 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-ACCT-0009` | `ACCOUNTING-INTERFACE` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-001 lines 2326–2342 | 08 master; deep 10 |
| `REQ-INFRA-0006` | `CROSS-DOMAIN` | `CALIBRATED` | `DEEP_SPEC` | SRC-001 lines 2343–2360 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-GRAPH-0007` | `CROSS-DOMAIN` | `RESEARCH` | `CROSS_DOMAIN_PASS08` | SRC-001 lines 2475–2502 | PASS08 Market Graph/Routes/Atlas |
| `REQ-CAP-0005` | `CAPITAL-OWNED` | `CALIBRATED` | `MASTER` | SRC-001 lines 2526–2577 | 08 master; deep 03–05/10 |
| `REQ-EXEC-0020` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-001 lines 2578–2634 | source provenance / owning domain research |
| `REQ-EXEC-0021` | `CROSS-DOMAIN` | `EXTERNAL_REVALIDATION` | `RESEARCH/FUTURE` | SRC-001 lines 2635–2669 | source provenance / owning domain research |
| `REQ-HWC-0009` | `CROSS-DOMAIN` | `RESEARCH` | `CROSS_DOMAIN_PASS08` | SRC-001 lines 2888–2971 | PASS08 Market Graph/Routes/Atlas |
| `REQ-ARCH-0009` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-001 lines 2972–3015 | source provenance / owning domain research |
| `REQ-INFRA-0008` | `CROSS-DOMAIN` | `CALIBRATED` | `DEEP_SPEC` | SRC-001 lines 3062–3126 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-INV-0002` | `INVENTORY-OWNED` | `EXTERNAL_REVALIDATION` | `RESEARCH/FUTURE` | SRC-001 lines 3128–3146 | 08 master; deep 01–03 |
| `REQ-EXEC-0022` | `CROSS-DOMAIN` | `CALIBRATED` | `DEEP_SPEC` | SRC-001 lines 3173–3264 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0023` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-001 lines 3265–3303 | source provenance / owning domain research |
| `REQ-DATA-0003` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-001 lines 3359–3407 | source provenance / owning domain research |
| `REQ-ATLAS-0001` | `CROSS-DOMAIN` | `RESEARCH` | `CROSS_DOMAIN_PASS08` | SRC-001 lines 3408–3452 | PASS08 Market Graph/Routes/Atlas |
| `REQ-REPLAY-0004` | `CROSS-DOMAIN` | `FUTURE` | `RESEARCH/FUTURE` | SRC-001 lines 3453–3492 | source provenance / owning domain research |
| `REQ-CAP-0006` | `CAPITAL-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-001 lines 3493–3550 | 08 master; deep 03–05/10 |
| `REQ-DATA-0004` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-001 lines 3551–3555 | source provenance / owning domain research |
| `REQ-BRIDGE-0004` | `BRIDGE-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-001 lines 3571–3577 | 08 master; deep 04–05/09 |
| `REQ-CAP-0007` | `CAPITAL-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-001 lines 3578–3584 | 08 master; deep 03–05/10 |
| `REQ-RISK-0013` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-001 lines 3592–3615 | source provenance / owning domain research |
| `REQ-INFRA-0009` | `CROSS-DOMAIN` | `CALIBRATED` | `DEEP_SPEC` | SRC-001 lines 3616–3658 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0009` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-001 lines 3683–3710 | source provenance / owning domain research |
| `REQ-MICRO-0001` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-002 lines 418–427 | source provenance / owning domain research |
| `REQ-EXEC-0026` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-002 lines 428–436 | source provenance / owning domain research |
| `REQ-MICRO-0002` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-002 lines 846–897 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0033` | `CROSS-DOMAIN` | `REJECTED` | `DEEP_SPEC` | SRC-002 lines 1256–1276 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-ACCT-0011` | `ACCOUNTING-INTERFACE` | `EXTERNAL_REVALIDATION` | `RESEARCH/FUTURE` | SRC-002 lines 1293–1313 | 08 master; deep 10 |
| `REQ-ARCH-0020` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-002 lines 1314–1350 | source provenance / owning domain research |
| `REQ-INV-0003` | `INVENTORY-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-002 lines 1353–1366 | 08 master; deep 01–03 |
| `REQ-INV-0004` | `INVENTORY-OWNED` | `EXTERNAL_REVALIDATION` | `RESEARCH/FUTURE` | SRC-002 lines 1372–1377 | 08 master; deep 01–03 |
| `REQ-RISK-0015` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-002 lines 1406–1439 | source provenance / owning domain research |
| `REQ-CAP-0008` | `CAPITAL-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-002 lines 1591–1601 | 08 master; deep 03–05/10 |
| `REQ-INFRA-0012` | `CROSS-DOMAIN` | `FUTURE` | `RESEARCH/FUTURE` | SRC-002 lines 1602–1636 | source provenance / owning domain research |
| `REQ-EXEC-0038` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-002 lines 1637–1664 | source provenance / owning domain research |
| `REQ-CAP-0009` | `CAPITAL-OWNED` | `REJECTED` | `MASTER` | SRC-002 lines 1665–1675 | 08 master; deep 03–05/10 |
| `REQ-CAP-0010` | `CAPITAL-OWNED` | `LOCKED` | `MASTER` | SRC-002 lines 1676–1694 | 08 master; deep 03–05/10 |
| `REQ-EXEC-0039` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-002 lines 1695–1726 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-ROUTE-0008` | `CROSS-DOMAIN` | `RESEARCH` | `CROSS_DOMAIN_PASS08` | SRC-002 lines 1819–1840 | PASS08 Market Graph/Routes/Atlas |
| `REQ-ROUTE-0009` | `CROSS-DOMAIN` | `EXTERNAL_REVALIDATION` | `CROSS_DOMAIN_PASS08` | SRC-002 lines 1841–1851 | PASS08 Market Graph/Routes/Atlas |
| `REQ-ACCT-0012` | `ACCOUNTING-INTERFACE` | `LOCKED` | `MASTER` | SRC-002 lines 1852–1866 | 08 master; deep 10 |
| `REQ-ACCT-0014` | `ACCOUNTING-INTERFACE` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-002 lines 1896–1902 | 08 master; deep 10 |
| `REQ-EXEC-0042` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-002 lines 1912–1935 | source provenance / owning domain research |
| `REQ-RISK-0016` | `CROSS-DOMAIN` | `FUTURE` | `RESEARCH/FUTURE` | SRC-002 lines 1936–1945 | source provenance / owning domain research |
| `REQ-ACCT-0016` | `ACCOUNTING-INTERFACE` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-002 lines 1946–1958 | 08 master; deep 10 |
| `REQ-ACCT-0017` | `ACCOUNTING-INTERFACE` | `LOCKED` | `MASTER` | SRC-002 lines 1959–1982 | 08 master; deep 10 |
| `REQ-RISK-0017` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-002 lines 1983–1999 | source provenance / owning domain research |
| `REQ-RISK-0020` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-002 lines 2005–2006 | source provenance / owning domain research |
| `REQ-RECOV-0007` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-002 lines 2010–2034 | source provenance / owning domain research |
| `REQ-ROUTE-0010` | `CROSS-DOMAIN` | `EXTERNAL_REVALIDATION` | `CROSS_DOMAIN_PASS08` | SRC-002 lines 2036–2039 | PASS08 Market Graph/Routes/Atlas |
| `REQ-ACCT-0019` | `ACCOUNTING-INTERFACE` | `LOCKED` | `MASTER` | SRC-002 lines 2040–2065 | 08 master; deep 10 |
| `REQ-EXEC-0043` | `CROSS-DOMAIN` | `EXTERNAL_REVALIDATION` | `RESEARCH/FUTURE` | SRC-002 lines 2066–2164 | source provenance / owning domain research |
| `REQ-ROUTE-0011` | `CROSS-DOMAIN` | `RESEARCH` | `CROSS_DOMAIN_PASS08` | SRC-002 lines 2253–2283 | PASS08 Market Graph/Routes/Atlas |
| `REQ-INV-0005` | `INVENTORY-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-002 lines 2336–2353 | 08 master; deep 01–03 |
| `REQ-INV-0006` | `INVENTORY-OWNED` | `EXTERNAL_REVALIDATION` | `RESEARCH/FUTURE` | SRC-002 lines 2369–2436 | 08 master; deep 01–03 |
| `REQ-INFRA-0014` | `CROSS-DOMAIN` | `EXTERNAL_REVALIDATION` | `RESEARCH/FUTURE` | SRC-002 lines 2475–2511 | source provenance / owning domain research |
| `REQ-INV-0007` | `INVENTORY-OWNED` | `EXTERNAL_REVALIDATION` | `RESEARCH/FUTURE` | SRC-002 lines 2526–2527 | 08 master; deep 01–03 |
| `REQ-INFRA-0015` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-002 lines 2547–2582 | source provenance / owning domain research |
| `REQ-CAP-0011` | `CAPITAL-OWNED` | `LOCKED` | `MASTER` | SRC-002 lines 2583–2601 | 08 master; deep 03–05/10 |
| `REQ-CAP-0012` | `CAPITAL-OWNED` | `LOCKED` | `MASTER` | SRC-002 lines 2602–2614 | 08 master; deep 03–05/10 |
| `REQ-FUTURE-0004` | `CROSS-DOMAIN` | `FUTURE` | `RESEARCH/FUTURE` | SRC-002 lines 2657–2673 | source provenance / owning domain research |
| `REQ-QUANT-0003` | `CROSS-DOMAIN` | `LOCKED` | `CROSS_DOMAIN_PASS08` | SRC-002 lines 2674–2704 | PASS08 Market Graph/Routes/Atlas |
| `REQ-CAP-0013` | `CAPITAL-OWNED` | `REJECTED` | `MASTER` | SRC-002 lines 2705–2749 | 08 master; deep 03–05/10 |
| `REQ-HWC-0016` | `CROSS-DOMAIN` | `FUTURE` | `CROSS_DOMAIN_PASS08` | SRC-002 lines 2750–2798 | PASS08 Market Graph/Routes/Atlas |
| `REQ-CAP-0014` | `CAPITAL-OWNED` | `FUTURE` | `RESEARCH/FUTURE` | SRC-002 lines 2816–2821 | 08 master; deep 03–05/10 |
| `REQ-ACCT-0021` | `ACCOUNTING-INTERFACE` | `LOCKED` | `MASTER` | SRC-002 lines 2845–2888 | 08 master; deep 10 |
| `REQ-ACCT-0024` | `ACCOUNTING-INTERFACE` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-002 lines 3000–3008 | 08 master; deep 10 |
| `REQ-EXEC-0048` | `CROSS-DOMAIN` | `FUTURE` | `RESEARCH/FUTURE` | SRC-002 lines 3018–3049 | source provenance / owning domain research |
| `REQ-BRIDGE-0005` | `BRIDGE-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-002 lines 3102–3126 | 08 master; deep 04–05/09 |
| `REQ-HWC-0019` | `CROSS-DOMAIN` | `RESEARCH` | `CROSS_DOMAIN_PASS08` | SRC-002 lines 3157–3165 | PASS08 Market Graph/Routes/Atlas |
| `REQ-HWC-0020` | `CROSS-DOMAIN` | `RESEARCH` | `CROSS_DOMAIN_PASS08` | SRC-002 lines 3166–3176 | PASS08 Market Graph/Routes/Atlas |
| `REQ-ACCT-0025` | `ACCOUNTING-INTERFACE` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-002 lines 3177–3213 | 08 master; deep 10 |
| `REQ-EXEC-0049` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-002 lines 3214–3251 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-ACCT-0026` | `ACCOUNTING-INTERFACE` | `FUTURE` | `RESEARCH/FUTURE` | SRC-002 lines 3275–3327 | 08 master; deep 10 |
| `REQ-HWC-0023` | `CROSS-DOMAIN` | `RESEARCH` | `CROSS_DOMAIN_PASS08` | SRC-002 lines 3339–3341 | PASS08 Market Graph/Routes/Atlas |
| `REQ-RISK-0023` | `CROSS-DOMAIN` | `REJECTED` | `DEEP_SPEC` | SRC-002 lines 3359–3380 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0024` | `CROSS-DOMAIN` | `FUTURE` | `RESEARCH/FUTURE` | SRC-002 lines 3518–3530 | source provenance / owning domain research |
| `REQ-EXEC-0051` | `CROSS-DOMAIN` | `EXTERNAL_REVALIDATION` | `RESEARCH/FUTURE` | SRC-002 lines 3640–3697 | source provenance / owning domain research |
| `REQ-HWC-0025` | `CROSS-DOMAIN` | `RESEARCH` | `CROSS_DOMAIN_PASS08` | SRC-002 lines 3799–3820 | PASS08 Market Graph/Routes/Atlas |
| `REQ-REPLAY-0005` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-002 lines 4421–4478 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-ARCH-0035` | `CROSS-DOMAIN` | `CALIBRATED` | `DEEP_SPEC` | SRC-002 lines 4479–4529 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-HWC-0026` | `CROSS-DOMAIN` | `LOCKED` | `CROSS_DOMAIN_PASS08` | SRC-002 lines 4560–4619 | PASS08 Market Graph/Routes/Atlas |
| `REQ-ACCT-0029` | `ACCOUNTING-INTERFACE` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-002 lines 4620–4644 | 08 master; deep 10 |
| `REQ-ARCH-0036` | `CROSS-DOMAIN` | `FUTURE` | `RESEARCH/FUTURE` | SRC-002 lines 4847–4868 | source provenance / owning domain research |
| `REQ-EXEC-0055` | `CROSS-DOMAIN` | `EXTERNAL_REVALIDATION` | `RESEARCH/FUTURE` | SRC-002 lines 4875–4991 | source provenance / owning domain research |
| `REQ-EXEC-0056` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-002 lines 5012–5047 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-ACCT-0030` | `ACCOUNTING-INTERFACE` | `LOCKED` | `MASTER` | SRC-002 lines 5048–5072 | 08 master; deep 10 |
| `REQ-BRIDGE-0006` | `BRIDGE-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-002 lines 5276–5309 | 08 master; deep 04–05/09 |
| `REQ-EXEC-0057` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-002 lines 5310–5392 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-CLOCK-0003` | `CROSS-DOMAIN` | `REJECTED` | `DEEP_SPEC` | SRC-002 lines 5585–5676 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-ARCH-0041` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-002 lines 5854–5899 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-ARCH-0042` | `CROSS-DOMAIN` | `CALIBRATED` | `DEEP_SPEC` | SRC-002 lines 5941–5973 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0027` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-002 lines 6017–6051 | source provenance / owning domain research |
| `REQ-EXEC-0062` | `CROSS-DOMAIN` | `EXTERNAL_REVALIDATION` | `RESEARCH/FUTURE` | SRC-003 lines 1–30 | source provenance / owning domain research |
| `REQ-ACCT-0031` | `ACCOUNTING-INTERFACE` | `CALIBRATED` | `MASTER` | SRC-003 lines 52–76 | 08 master; deep 10 |
| `REQ-EXEC-0064` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-003 lines 77–118 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-ACCT-0032` | `ACCOUNTING-INTERFACE` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 335–388 | 08 master; deep 10 |
| `REQ-DATA-0007` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 493–519 | source provenance / owning domain research |
| `REQ-RISK-0028` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 520–568 | source provenance / owning domain research |
| `REQ-INFRA-0031` | `CROSS-DOMAIN` | `CALIBRATED` | `DEEP_SPEC` | SRC-003 lines 587–619 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-INV-0008` | `INVENTORY-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 701–711 | 08 master; deep 01–03 |
| `REQ-EXEC-0071` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 958–972 | source provenance / owning domain research |
| `REQ-ATLAS-0002` | `CROSS-DOMAIN` | `RESEARCH` | `CROSS_DOMAIN_PASS08` | SRC-003 lines 1028–1050 | PASS08 Market Graph/Routes/Atlas |
| `REQ-OPS-0004` | `CROSS-DOMAIN` | `CALIBRATED` | `DEEP_SPEC` | SRC-003 lines 1080–1125 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0074` | `CROSS-DOMAIN` | `CALIBRATED` | `DEEP_SPEC` | SRC-003 lines 1254–1283 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0075` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 1284–1338 | source provenance / owning domain research |
| `REQ-EXEC-0076` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 1357–1385 | source provenance / owning domain research |
| `REQ-BRIDGE-0007` | `BRIDGE-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 1386–1395 | 08 master; deep 04–05/09 |
| `REQ-RISK-0029` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 1400–1412 | source provenance / owning domain research |
| `REQ-RISK-0030` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 1413–1428 | source provenance / owning domain research |
| `REQ-ARCH-0064` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 1509–1534 | source provenance / owning domain research |
| `REQ-EXEC-0080` | `CROSS-DOMAIN` | `CALIBRATED` | `DEEP_SPEC` | SRC-003 lines 1596–1612 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0083` | `CROSS-DOMAIN` | `EXTERNAL_REVALIDATION` | `RESEARCH/FUTURE` | SRC-003 lines 1895–1939 | source provenance / owning domain research |
| `REQ-CAP-0015` | `CAPITAL-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 1940–1941 | 08 master; deep 03–05/10 |
| `REQ-RISK-0034` | `CROSS-DOMAIN` | `EXTERNAL_REVALIDATION` | `RESEARCH/FUTURE` | SRC-003 lines 1948–1968 | source provenance / owning domain research |
| `REQ-RISK-0035` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 1969–1988 | source provenance / owning domain research |
| `REQ-SEC-0002` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 2011–2045 | source provenance / owning domain research |
| `REQ-GRAPH-0013` | `CROSS-DOMAIN` | `FUTURE` | `CROSS_DOMAIN_PASS08` | SRC-003 lines 2048–2104 | PASS08 Market Graph/Routes/Atlas |
| `REQ-ACCT-0036` | `ACCOUNTING-INTERFACE` | `FUTURE` | `RESEARCH/FUTURE` | SRC-003 lines 2105–2120 | 08 master; deep 10 |
| `REQ-EXEC-0085` | `CROSS-DOMAIN` | `EXTERNAL_REVALIDATION` | `RESEARCH/FUTURE` | SRC-003 lines 2184–2214 | source provenance / owning domain research |
| `REQ-OWA-0004` | `CROSS-DOMAIN` | `RESEARCH` | `CROSS_DOMAIN_PASS08` | SRC-003 lines 2562–2596 | PASS08 Market Graph/Routes/Atlas |
| `REQ-BRIDGE-0008` | `BRIDGE-OWNED` | `FUTURE` | `RESEARCH/FUTURE` | SRC-003 lines 2597–2615 | 08 master; deep 04–05/09 |
| `REQ-BRIDGE-0009` | `BRIDGE-OWNED` | `FUTURE` | `RESEARCH/FUTURE` | SRC-003 lines 2628–2641 | 08 master; deep 04–05/09 |
| `REQ-INV-0009` | `INVENTORY-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 2661–2674 | 08 master; deep 01–03 |
| `REQ-INV-0010` | `INVENTORY-OWNED` | `FUTURE` | `RESEARCH/FUTURE` | SRC-003 lines 2675–2689 | 08 master; deep 01–03 |
| `REQ-BRIDGE-0010` | `BRIDGE-OWNED` | `REJECTED` | `MASTER` | SRC-003 lines 2722–2750 | 08 master; deep 04–05/09 |
| `REQ-ACCT-0041` | `ACCOUNTING-INTERFACE` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 2766–2790 | 08 master; deep 10 |
| `REQ-INV-0011` | `INVENTORY-OWNED` | `CALIBRATED` | `MASTER` | SRC-003 lines 2791–2811 | 08 master; deep 01–03 |
| `REQ-RISK-0036` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 2812–2843 | source provenance / owning domain research |
| `REQ-ROUTE-0026` | `CROSS-DOMAIN` | `RESEARCH` | `CROSS_DOMAIN_PASS08` | SRC-003 lines 2868–2888 | PASS08 Market Graph/Routes/Atlas |
| `REQ-ACCT-0042` | `ACCOUNTING-INTERFACE` | `LOCKED` | `MASTER` | SRC-003 lines 2889–2905 | 08 master; deep 10 |
| `REQ-RECOV-0011` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 2994–3019 | source provenance / owning domain research |
| `REQ-SIZE-0001` | `SIZING-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 3047–3070 | 08 master; deep 06–07 |
| `REQ-SIZE-0002` | `SIZING-OWNED` | `EXTERNAL_REVALIDATION` | `RESEARCH/FUTURE` | SRC-003 lines 3084–3100 | 08 master; deep 06–07 |
| `REQ-SLICE-0001` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 3120–3141 | source provenance / owning domain research |
| `REQ-SLICE-0002` | `CROSS-DOMAIN` | `REJECTED` | `REJECTED` | SRC-003 lines 3142–3161 | CONFLICT_RESOLUTION.md / source history |
| `REQ-CAP-0016` | `CAPITAL-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 3162–3187 | 08 master; deep 03–05/10 |
| `REQ-INV-0012` | `INVENTORY-OWNED` | `LOCKED` | `MASTER` | SRC-003 lines 3188–3205 | 08 master; deep 01–03 |
| `REQ-ROUTE-0027` | `CROSS-DOMAIN` | `FUTURE` | `CROSS_DOMAIN_PASS08` | SRC-003 lines 3206–3236 | PASS08 Market Graph/Routes/Atlas |
| `REQ-INV-0013` | `INVENTORY-OWNED` | `FUTURE` | `RESEARCH/FUTURE` | SRC-003 lines 3315–3330 | 08 master; deep 01–03 |
| `REQ-VALID-0013` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 3331–3345 | source provenance / owning domain research |
| `REQ-VALID-0014` | `CROSS-DOMAIN` | `REJECTED` | `RESEARCH/FUTURE` | SRC-003 lines 3346–3372 | source provenance / owning domain research |
| `REQ-XEX-0005` | `CROSS-DOMAIN` | `EXTERNAL_REVALIDATION` | `RESEARCH/FUTURE` | SRC-003 lines 3373–3393 | source provenance / owning domain research |
| `REQ-ACCT-0044` | `ACCOUNTING-INTERFACE` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 3421–3447 | 08 master; deep 10 |
| `REQ-ACCT-0045` | `ACCOUNTING-INTERFACE` | `FUTURE` | `RESEARCH/FUTURE` | SRC-003 lines 3448–3464 | 08 master; deep 10 |
| `REQ-EXEC-0093` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 3465–3500 | source provenance / owning domain research |
| `REQ-EXEC-0094` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-003 lines 3501–3543 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RECOV-0012` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-003 lines 3544–3566 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RECOV-0013` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-003 lines 3624–3656 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RECOV-0014` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-003 lines 3657–3691 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0095` | `CROSS-DOMAIN` | `FUTURE` | `RESEARCH/FUTURE` | SRC-003 lines 3692–3759 | source provenance / owning domain research |
| `REQ-RISK-0041` | `CROSS-DOMAIN` | `EXTERNAL_REVALIDATION` | `RESEARCH/FUTURE` | SRC-003 lines 3798–3852 | source provenance / owning domain research |
| `REQ-INV-0014` | `INVENTORY-OWNED` | `FUTURE` | `RESEARCH/FUTURE` | SRC-003 lines 3853–3890 | 08 master; deep 01–03 |
| `REQ-RISK-0042` | `CROSS-DOMAIN` | `EXTERNAL_REVALIDATION` | `RESEARCH/FUTURE` | SRC-003 lines 3891–3928 | source provenance / owning domain research |
| `REQ-INV-0015` | `INVENTORY-OWNED` | `FUTURE` | `RESEARCH/FUTURE` | SRC-003 lines 3929–3961 | 08 master; deep 01–03 |
| `REQ-INV-0016` | `INVENTORY-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 3962–3971 | 08 master; deep 01–03 |
| `REQ-RISK-0043` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 3972–3980 | source provenance / owning domain research |
| `REQ-INV-0017` | `INVENTORY-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 3981–3991 | 08 master; deep 01–03 |
| `REQ-INV-0018` | `INVENTORY-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 3992–4027 | 08 master; deep 01–03 |
| `REQ-INFRA-0034` | `CROSS-DOMAIN` | `CALIBRATED` | `DEEP_SPEC` | SRC-003 lines 4028–4054 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-ATLAS-0003` | `CROSS-DOMAIN` | `LOCKED` | `CROSS_DOMAIN_PASS08` | SRC-003 lines 4055–4079 | PASS08 Market Graph/Routes/Atlas |
| `REQ-INV-0019` | `INVENTORY-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 4104–4105 | 08 master; deep 01–03 |
| `REQ-RISK-0045` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 4110–4132 | source provenance / owning domain research |
| `REQ-CAP-0017` | `CAPITAL-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 4133–4144 | 08 master; deep 03–05/10 |
| `REQ-ACCT-0046` | `ACCOUNTING-INTERFACE` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 4165–4189 | 08 master; deep 10 |
| `REQ-ACCT-0047` | `ACCOUNTING-INTERFACE` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 4190–4209 | 08 master; deep 10 |
| `REQ-ACCT-0048` | `ACCOUNTING-INTERFACE` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-003 lines 4210–4232 | 08 master; deep 10 |
| `REQ-EXEC-0097` | `CROSS-DOMAIN` | `FUTURE` | `RESEARCH/FUTURE` | SRC-003 lines 4233–4272 | source provenance / owning domain research |
| `REQ-EXEC-0104` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 152–188 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0107` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 225–256 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0110` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 309–324 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0112` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 355–457 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0131` | `CROSS-DOMAIN` | `REJECTED` | `DEEP_SPEC` | SRC-004 lines 883–914 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0132` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 915–934 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0135` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 982–991 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0136` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 992–1013 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0140` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 1064–1088 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0142` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 1125–1138 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0144` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 1174–1185 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0148` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 1265–1286 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0150` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 1302–1320 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0153` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 1354–1370 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0156` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 1398–1417 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0157` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 1418–1437 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0161` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 1493–1519 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0165` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 1579–1594 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0166` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 1595–1679 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0167` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 1680–1692 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0174` | `CROSS-DOMAIN` | `OPEN` | `DEEP_SPEC` | SRC-004 lines 1799–1822 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0175` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 1823–1904 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0178` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 1957–1977 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0188` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 2208–2218 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0199` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 2520–2532 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0204` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 2600–2627 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0207` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 2681–2715 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0209` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 2731–2746 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0214` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 2807–2814 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0217` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 2852–2869 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0219` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 2879–2899 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0221` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 2919–2937 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0227` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 3040–3052 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0228` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 3053–3068 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0239` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-004 lines 3218–3309 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-FORMULA-0003` | `CROSS-DOMAIN` | `LOCKED` | `FORMULA_REFERENCE` | SRC-004 lines 3312–3398 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0018` | `CROSS-DOMAIN` | `LOCKED` | `FORMULA_REFERENCE` | SRC-004 lines 3710–3718 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0041` | `CROSS-DOMAIN` | `LOCKED` | `FORMULA_REFERENCE` | SRC-004 lines 4804–4859 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0042` | `CROSS-DOMAIN` | `LOCKED` | `FORMULA_REFERENCE` | SRC-004 lines 4860–4925 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0078` | `CROSS-DOMAIN` | `CALIBRATED` | `FORMULA_REFERENCE` | SRC-004 lines 6392–6491 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0079` | `INVENTORY-OWNED` | `LOCKED` | `FORMULA_REFERENCE` | SRC-004 lines 6492–6517 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0080` | `INVENTORY-OWNED` | `CALIBRATED` | `FORMULA_REFERENCE` | SRC-004 lines 6518–6542 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0081` | `INVENTORY-OWNED` | `LOCKED` | `FORMULA_REFERENCE` | SRC-004 lines 6543–6589 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0083` | `BRIDGE-OWNED` | `LOCKED` | `FORMULA_REFERENCE` | SRC-004 lines 6623–6692 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0084` | `CAPITAL-OWNED` | `CALIBRATED` | `FORMULA_REFERENCE` | SRC-004 lines 6693–6763 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0085` | `BRIDGE-OWNED` | `LOCKED` | `FORMULA_REFERENCE` | SRC-004 lines 6764–6820 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0086` | `BRIDGE-OWNED` | `LOCKED` | `FORMULA_REFERENCE` | SRC-004 lines 6821–6886 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0087` | `BRIDGE-OWNED` | `LOCKED` | `FORMULA_REFERENCE` | SRC-004 lines 6887–7003 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0088` | `SIZING-OWNED` | `LOCKED` | `FORMULA_REFERENCE` | SRC-004 lines 7004–7078 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0089` | `SIZING-OWNED` | `LOCKED` | `FORMULA_REFERENCE` | SRC-004 lines 7079–7140 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0090` | `SIZING-OWNED` | `LOCKED` | `FORMULA_REFERENCE` | SRC-004 lines 7141–7273 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0091` | `SIZING-OWNED` | `LOCKED` | `FORMULA_REFERENCE` | SRC-004 lines 7274–7313 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0092` | `SIZING-OWNED` | `LOCKED` | `FORMULA_REFERENCE` | SRC-004 lines 7314–7342 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0093` | `PORTFOLIO-OWNED` | `LOCKED` | `FORMULA_REFERENCE` | SRC-004 lines 7343–7380 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0094` | `ACCOUNTING-INTERFACE` | `LOCKED` | `FORMULA_REFERENCE` | SRC-004 lines 7381–7468 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0095` | `ACCOUNTING-INTERFACE` | `LOCKED` | `FORMULA_REFERENCE` | SRC-004 lines 7469–7546 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0101` | `CROSS-DOMAIN` | `LOCKED` | `FORMULA_REFERENCE` | SRC-004 lines 7802–7855 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0115` | `CROSS-DOMAIN` | `LOCKED` | `FORMULA_REFERENCE` | SRC-004 lines 8560–8611 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0120` | `ACCOUNTING-INTERFACE` | `CALIBRATED` | `FORMULA_REFERENCE` | SRC-004 lines 8833–8890 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0121` | `ACCOUNTING-INTERFACE` | `LOCKED` | `FORMULA_REFERENCE` | SRC-004 lines 8891–8984 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0122` | `ACCOUNTING-INTERFACE` | `LOCKED` | `FORMULA_REFERENCE` | SRC-004 lines 8985–9048 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0123` | `ACCOUNTING-INTERFACE` | `LOCKED` | `FORMULA_REFERENCE` | SRC-004 lines 9049–9147 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0125` | `CROSS-DOMAIN` | `LOCKED` | `FORMULA_REFERENCE` | SRC-004 lines 9205–9224 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0127` | `CROSS-DOMAIN` | `LOCKED` | `FORMULA_REFERENCE` | SRC-004 lines 9239–9284 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0130` | `CROSS-DOMAIN` | `LOCKED` | `FORMULA_REFERENCE` | SRC-004 lines 9354–9370 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0135` | `CROSS-DOMAIN` | `LOCKED` | `FORMULA_REFERENCE` | SRC-004 lines 9513–9537 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0136` | `CROSS-DOMAIN` | `LOCKED` | `FORMULA_REFERENCE` | SRC-004 lines 9538–9587 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0137` | `CROSS-DOMAIN` | `LOCKED` | `FORMULA_REFERENCE` | SRC-004 lines 9588–9777 | FORMULA_INDEX.md / PASS11 |
| `REQ-RISK-0050` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 179–198 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0051` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 199–221 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0058` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 381–396 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0059` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 397–472 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0060` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 473–485 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0067` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 674–683 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0068` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 684–707 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0069` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 708–717 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0070` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 718–756 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0075` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 837–857 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0077` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 870–883 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0086` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 1089–1120 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0099` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 1485–1497 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0105` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 1668–1723 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0108` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 1757–1807 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0109` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 1808–1823 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0111` | `CROSS-DOMAIN` | `FUTURE` | `DEEP_SPEC` | SRC-005 lines 1862–1910 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0112` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 1911–1928 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0114` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 1954–2027 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0115` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 2028–2077 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0116` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 2078–2090 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0117` | `CROSS-DOMAIN` | `FUTURE` | `DEEP_SPEC` | SRC-005 lines 2091–2111 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0118` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 2112–2141 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0119` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 2142–2155 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0120` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 2156–2171 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0127` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 2342–2357 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0133` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 2485–2512 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0134` | `CROSS-DOMAIN` | `OPEN` | `DEEP_SPEC` | SRC-005 lines 2513–2569 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0135` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 2570–2593 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0136` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 2594–2604 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0137` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 2605–2644 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0138` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 2645–2652 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0140` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 2664–2672 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0165` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 3044–3058 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0166` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 3059–3070 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0167` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 3071–3084 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0170` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 3101–3110 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0171` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 3111–3123 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0190` | `CROSS-DOMAIN` | `REJECTED` | `DEEP_SPEC` | SRC-005 lines 3366–3383 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0191` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 3384–3398 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0200` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 3456–3474 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0202` | `CROSS-DOMAIN` | `REJECTED` | `DEEP_SPEC` | SRC-005 lines 3505–3517 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0204` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 3531–3545 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0205` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 3546–3586 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0207` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 3597–3605 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0218` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 3769–3783 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0222` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 3847–3859 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0223` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 3860–3874 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0230` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 3946–3957 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0231` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 3958–3969 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0243` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 4113–4147 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0245` | `CROSS-DOMAIN` | `FUTURE` | `DEEP_SPEC` | SRC-005 lines 4178–4211 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0256` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 4339–4355 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0257` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 4356–4395 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0258` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 4396–4428 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0259` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 4429–4442 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0260` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 4443–4458 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0267` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 4595–4609 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0268` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 4610–4627 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0269` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 4628–4651 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0276` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 4735–4746 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0279` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 4815–4876 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0280` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 4877–4894 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0281` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 4895–4904 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0284` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 4942–4958 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0295` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 5081–5131 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0296` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 5132–5185 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0013` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 5451–5462 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0014` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 5463–5472 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0015` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 5473–5482 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0025` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 5661–5676 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0026` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 5677–5692 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0028` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 5707–5729 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0039` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 5879–5891 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0043` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 5953–5990 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0044` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 5991–6006 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0046` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 6014–6031 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0047` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 6032–6042 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0048` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 6043–6060 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0049` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 6061–6072 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0050` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 6073–6087 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0051` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 6088–6104 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0054` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 6138–6149 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0063` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 6276–6295 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0072` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 6433–6455 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0078` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 6561–6571 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0095` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 6827–6842 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0129` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 7491–7500 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0137` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 7590–7602 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0146` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 7726–7733 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0148` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 7752–7766 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0152` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 7813–7824 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0153` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 7825–7841 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0155` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 7852–7865 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0156` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 7866–7882 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-REPLAY-0011` | `CROSS-DOMAIN` | `FUTURE` | `RESEARCH/FUTURE` | SRC-005 lines 7996–8013 | source provenance / owning domain research |
| `REQ-DATA-0190` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 8312–8324 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0200` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 8423–8430 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0206` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 8494–8503 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0215` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 8625–8634 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0222` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 8682–8692 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0297` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 9457–9467 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0301` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 9513–9539 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0310` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 9681–9692 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DATA-0313` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-005 lines 9719–9744 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DEPLOY-0002` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 5–40 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DEPLOY-0033` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 604–615 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DEPLOY-0035` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 627–651 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DEPLOY-0037` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 681–689 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DEPLOY-0043` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 749–761 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DEPLOY-0046` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 782–792 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DEPLOY-0114` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 1723–1732 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DEPLOY-0118` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 1748–1750 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-CLIENT-0011` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 2135–2144 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-OPS-0017` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 2748–2754 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-DEPLOY-0215` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 3545–3594 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0021` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 3676–3687 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0022` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 3688–3702 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0025` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 3729–3741 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0036` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 3894–3901 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0050` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4008–4016 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0055` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4059–4066 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0058` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4097–4103 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0065` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4176–4186 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0067` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4192–4197 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0068` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4198–4204 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0076` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4258–4268 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0093` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4374–4383 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0094` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4384–4387 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0095` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4388–4392 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0096` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4393–4396 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0097` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4397–4404 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0098` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4405–4411 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0099` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4412–4416 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0100` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4417–4422 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0102` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4426–4466 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0103` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4467–4471 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0104` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4472–4479 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0107` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4486–4491 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0108` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4492–4494 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0109` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4495–4514 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0110` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4515–4520 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0112` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4528–4532 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0114` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4537–4539 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0120` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4563–4565 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0126` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4590–4603 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0136` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4642–4650 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0153` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4756–4758 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0154` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4759–4763 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0161` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4807–4813 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0162` | `CROSS-DOMAIN` | `CALIBRATED` | `DEEP_SPEC` | SRC-006 lines 4814–4821 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0181` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 4990–4996 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0183` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 5001–5006 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0209` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 5249–5251 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0211` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 5255–5257 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0222` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 5317–5329 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0227` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 5349–5356 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0279` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 5732–5740 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0286` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 5759–5764 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0287` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 5765–5775 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0290` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 5788–5805 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0292` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 5810–5812 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0364` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 6581–6595 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0365` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 6596–6672 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0366` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 6673–6743 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0367` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-006 lines 6744–6903 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-INFRA-0035` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 1–16 | source provenance / owning domain research |
| `REQ-QUANT-0006` | `CROSS-DOMAIN` | `RESEARCH` | `CROSS_DOMAIN_PASS08` | SRC-007 lines 17–28 | PASS08 Market Graph/Routes/Atlas |
| `REQ-INFRA-0036` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 29–57 | source provenance / owning domain research |
| `REQ-INFRA-0037` | `CROSS-DOMAIN` | `EXTERNAL_REVALIDATION` | `RESEARCH/FUTURE` | SRC-007 lines 58–103 | source provenance / owning domain research |
| `REQ-EXEC-0245` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-007 lines 1014–1056 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-EXEC-0246` | `CROSS-DOMAIN` | `EXTERNAL_REVALIDATION` | `RESEARCH/FUTURE` | SRC-007 lines 1057–1083 | source provenance / owning domain research |
| `REQ-MICRO-0007` | `CROSS-DOMAIN` | `EXTERNAL_REVALIDATION` | `RESEARCH/FUTURE` | SRC-007 lines 1158–1199 | source provenance / owning domain research |
| `REQ-MICRO-0009` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 1551–1676 | source provenance / owning domain research |
| `REQ-LIQ-0002` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 1677–1762 | source provenance / owning domain research |
| `REQ-SLICE-0003` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-007 lines 1763–1877 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-XMARKET-0006` | `CROSS-DOMAIN` | `RESEARCH` | `CROSS_DOMAIN_PASS08` | SRC-007 lines 2410–2469 | PASS08 Market Graph/Routes/Atlas |
| `REQ-EXEC-0253` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 2470–2488 | source provenance / owning domain research |
| `REQ-XMARKET-0008` | `CROSS-DOMAIN` | `RESEARCH` | `CROSS_DOMAIN_PASS08` | SRC-007 lines 2548–2560 | PASS08 Market Graph/Routes/Atlas |
| `REQ-SURV-0007` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-007 lines 2964–2999 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0300` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-007 lines 3300–3324 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0301` | `CROSS-DOMAIN` | `OPEN` | `OPEN_ITEM` | SRC-007 lines 3496–3514 | OPEN_ITEMS_INITIAL.md |
| `REQ-EXEC-0258` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 3860–3917 | source provenance / owning domain research |
| `REQ-ARCH-0076` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 4160–4181 | source provenance / owning domain research |
| `REQ-HWC-0028` | `CROSS-DOMAIN` | `RESEARCH` | `CROSS_DOMAIN_PASS08` | SRC-007 lines 4308–4309 | PASS08 Market Graph/Routes/Atlas |
| `REQ-PART-0012` | `CROSS-DOMAIN` | `FUTURE` | `RESEARCH/FUTURE` | SRC-007 lines 4353–4444 | source provenance / owning domain research |
| `REQ-PART-0013` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 4445–4519 | source provenance / owning domain research |
| `REQ-PART-0014` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 4581–4614 | source provenance / owning domain research |
| `REQ-PART-0015` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 4615–4646 | source provenance / owning domain research |
| `REQ-SURV-0015` | `CROSS-DOMAIN` | `REJECTED` | `DEEP_SPEC` | SRC-007 lines 4778–4800 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0302` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-007 lines 4877–4899 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0304` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 4932–5138 | source provenance / owning domain research |
| `REQ-EXEC-0265` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 5189–5206 | source provenance / owning domain research |
| `REQ-EXEC-0266` | `CROSS-DOMAIN` | `EXTERNAL_REVALIDATION` | `RESEARCH/FUTURE` | SRC-007 lines 5300–5309 | source provenance / owning domain research |
| `REQ-EXEC-0267` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-007 lines 5310–5342 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-QUANT-0010` | `CROSS-DOMAIN` | `LOCKED` | `CROSS_DOMAIN_PASS08` | SRC-007 lines 5389–5448 | PASS08 Market Graph/Routes/Atlas |
| `REQ-QUANT-0011` | `CROSS-DOMAIN` | `LOCKED` | `CROSS_DOMAIN_PASS08` | SRC-007 lines 5449–5502 | PASS08 Market Graph/Routes/Atlas |
| `REQ-RECOV-0017` | `CROSS-DOMAIN` | `FUTURE` | `RESEARCH/FUTURE` | SRC-007 lines 5515–5531 | source provenance / owning domain research |
| `REQ-RECOV-0018` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 5732–5742 | source provenance / owning domain research |
| `REQ-FORMULA-0141` | `CROSS-DOMAIN` | `RESEARCH` | `FORMULA_REFERENCE` | SRC-007 lines 6759–6805 | FORMULA_INDEX.md / PASS11 |
| `REQ-RECOV-0019` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 7092–7105 | source provenance / owning domain research |
| `REQ-SLICE-0004` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 7326–7416 | source provenance / owning domain research |
| `REQ-RISK-0313` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 7741–7773 | source provenance / owning domain research |
| `REQ-RISK-0314` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 7909–7942 | source provenance / owning domain research |
| `REQ-SIZE-0003` | `SIZING-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 7943–8086 | 08 master; deep 06–07 |
| `REQ-CAP-0018` | `CAPITAL-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 8087–8107 | 08 master; deep 03–05/10 |
| `REQ-PORT-0001` | `PORTFOLIO-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 8133–8148 | 08 master; deep 08 |
| `REQ-RISK-0315` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 8149–8267 | source provenance / owning domain research |
| `REQ-EXEC-0279` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 8268–8283 | source provenance / owning domain research |
| `REQ-INV-0020` | `INVENTORY-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 8284–8378 | 08 master; deep 01–03 |
| `REQ-INV-0021` | `INVENTORY-OWNED` | `LOCKED` | `MASTER` | SRC-007 lines 8379–8447 | 08 master; deep 01–03 |
| `REQ-PORT-0002` | `PORTFOLIO-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 8462–8557 | 08 master; deep 08 |
| `REQ-INV-0022` | `INVENTORY-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 8558–8633 | 08 master; deep 01–03 |
| `REQ-BRIDGE-0011` | `BRIDGE-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 8634–8701 | 08 master; deep 04–05/09 |
| `REQ-BRIDGE-0012` | `BRIDGE-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 8702–8781 | 08 master; deep 04–05/09 |
| `REQ-CAP-0019` | `CAPITAL-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 8782–8876 | 08 master; deep 03–05/10 |
| `REQ-ACCT-0059` | `ACCOUNTING-INTERFACE` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 8877–8917 | 08 master; deep 10 |
| `REQ-QUANT-0018` | `CROSS-DOMAIN` | `RESEARCH` | `CROSS_DOMAIN_PASS08` | SRC-007 lines 8975–8988 | PASS08 Market Graph/Routes/Atlas |
| `REQ-RISK-0316` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 9113–9162 | source provenance / owning domain research |
| `REQ-EXEC-0281` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 9163–9200 | source provenance / owning domain research |
| `REQ-FORMULA-0142` | `CROSS-DOMAIN` | `CALIBRATED` | `FORMULA_REFERENCE` | SRC-007 lines 9243–9268 | FORMULA_INDEX.md / PASS11 |
| `REQ-RISK-0317` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 9269–9294 | source provenance / owning domain research |
| `REQ-INFRA-0046` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-007 lines 9356–9398 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0318` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 9691–9825 | source provenance / owning domain research |
| `REQ-DATA-0319` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 9857–9881 | source provenance / owning domain research |
| `REQ-INV-0023` | `INVENTORY-OWNED` | `FUTURE` | `RESEARCH/FUTURE` | SRC-007 lines 9918–9970 | 08 master; deep 01–03 |
| `REQ-MICRO-0018` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 10205–10225 | source provenance / owning domain research |
| `REQ-ARCH-0084` | `CROSS-DOMAIN` | `CALIBRATED` | `DEEP_SPEC` | SRC-007 lines 10238–10252 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-VALID-0371` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 10297–10316 | source provenance / owning domain research |
| `REQ-ROUTE-0034` | `CROSS-DOMAIN` | `RESEARCH` | `CROSS_DOMAIN_PASS08` | SRC-007 lines 10356–10384 | PASS08 Market Graph/Routes/Atlas |
| `REQ-EXEC-0284` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-007 lines 10385–10513 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-RISK-0321` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 10514–10641 | source provenance / owning domain research |
| `REQ-MICRO-0019` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 10650–10651 | source provenance / owning domain research |
| `REQ-SIZE-0004` | `SIZING-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 10660–10661 | 08 master; deep 06–07 |
| `REQ-PORT-0003` | `PORTFOLIO-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 10662–10664 | 08 master; deep 08 |
| `REQ-PORT-0004` | `PORTFOLIO-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 10678–10692 | 08 master; deep 08 |
| `REQ-QUANT-0026` | `CROSS-DOMAIN` | `RESEARCH` | `CROSS_DOMAIN_PASS08` | SRC-007 lines 10807–10879 | PASS08 Market Graph/Routes/Atlas |
| `REQ-RISK-0324` | `CROSS-DOMAIN` | `FUTURE` | `RESEARCH/FUTURE` | SRC-007 lines 10880–10934 | source provenance / owning domain research |
| `REQ-FORMULA-0144` | `CROSS-DOMAIN` | `RESEARCH` | `FORMULA_REFERENCE` | SRC-007 lines 10935–11159 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0146` | `CROSS-DOMAIN` | `RESEARCH` | `FORMULA_REFERENCE` | SRC-007 lines 11211–11724 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0147` | `CROSS-DOMAIN` | `CALIBRATED` | `FORMULA_REFERENCE` | SRC-007 lines 11725–11912 | FORMULA_INDEX.md / PASS11 |
| `REQ-FORMULA-0150` | `CROSS-DOMAIN` | `CALIBRATED` | `FORMULA_REFERENCE` | SRC-007 lines 12205–12310 | FORMULA_INDEX.md / PASS11 |
| `REQ-MICRO-0021` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 12325–12336 | source provenance / owning domain research |
| `REQ-INV-0024` | `INVENTORY-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-007 lines 12351–12356 | 08 master; deep 01–03 |
| `REQ-EXEC-0291` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-008 lines 374–526 | source provenance / owning domain research |
| `REQ-EXEC-0292` | `CROSS-DOMAIN` | `EXTERNAL_REVALIDATION` | `RESEARCH/FUTURE` | SRC-008 lines 527–574 | source provenance / owning domain research |
| `REQ-MICRO-0022` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-008 lines 575–606 | source provenance / owning domain research |
| `REQ-QUANT-0030` | `CROSS-DOMAIN` | `EXTERNAL_REVALIDATION` | `CROSS_DOMAIN_PASS08` | SRC-008 lines 728–744 | PASS08 Market Graph/Routes/Atlas |
| `REQ-QUANT-0031` | `CROSS-DOMAIN` | `RESEARCH` | `CROSS_DOMAIN_PASS08` | SRC-008 lines 745–773 | PASS08 Market Graph/Routes/Atlas |
| `REQ-EXEC-0294` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-008 lines 774–810 | source provenance / owning domain research |
| `REQ-EXEC-0295` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-008 lines 811–841 | source provenance / owning domain research |
| `REQ-CAP-0020` | `CAPITAL-OWNED` | `CALIBRATED` | `MASTER` | SRC-008 lines 1445–1484 | 08 master; deep 03–05/10 |
| `REQ-EXEC-0307` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-008 lines 1485–1507 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-SLICE-0005` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-008 lines 1508–1509 | source provenance / owning domain research |
| `REQ-SLICE-0006` | `CROSS-DOMAIN` | `FUTURE` | `RESEARCH/FUTURE` | SRC-008 lines 1551–1609 | source provenance / owning domain research |
| `REQ-PART-0025` | `CROSS-DOMAIN` | `EXTERNAL_REVALIDATION` | `RESEARCH/FUTURE` | SRC-008 lines 1785–1798 | source provenance / owning domain research |
| `REQ-VALID-0375` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-008 lines 2023–2054 | source provenance / owning domain research |
| `REQ-EXEC-0317` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-008 lines 2220–2262 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-ROUTE-0037` | `CROSS-DOMAIN` | `RESEARCH` | `CROSS_DOMAIN_PASS08` | SRC-008 lines 2314–2351 | PASS08 Market Graph/Routes/Atlas |
| `REQ-SIZE-0005` | `SIZING-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-008 lines 2352–2431 | 08 master; deep 06–07 |
| `REQ-EXEC-0320` | `CROSS-DOMAIN` | `FUTURE` | `RESEARCH/FUTURE` | SRC-008 lines 2446–2463 | source provenance / owning domain research |
| `REQ-EXEC-0322` | `CROSS-DOMAIN` | `EXTERNAL_REVALIDATION` | `RESEARCH/FUTURE` | SRC-008 lines 2621–2640 | source provenance / owning domain research |
| `REQ-EXEC-0325` | `CROSS-DOMAIN` | `FUTURE` | `RESEARCH/FUTURE` | SRC-008 lines 2707–2748 | source provenance / owning domain research |
| `REQ-EXEC-0327` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-008 lines 2827–2861 | source provenance / owning domain research |
| `REQ-INFRA-0074` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-008 lines 4196–4227 | source provenance / owning domain research |
| `REQ-VALID-0378` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-008 lines 4413–4442 | source provenance / owning domain research |
| `REQ-INFRA-0077` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-008 lines 4650–4681 | source provenance / owning domain research |
| `REQ-INFRA-0078` | `CROSS-DOMAIN` | `FUTURE` | `RESEARCH/FUTURE` | SRC-008 lines 4706–4739 | source provenance / owning domain research |
| `REQ-CAP-0021` | `CAPITAL-OWNED` | `LOCKED` | `MASTER` | SRC-008 lines 5299–5356 | 08 master; deep 03–05/10 |
| `REQ-CAP-0022` | `CAPITAL-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-008 lines 5357–5385 | 08 master; deep 03–05/10 |
| `REQ-CLIENT-0025` | `CROSS-DOMAIN` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-008 lines 5860–5891 | source provenance / owning domain research |
| `REQ-CLIENT-0027` | `CROSS-DOMAIN` | `LOCKED` | `DEEP_SPEC` | SRC-008 lines 5990–6011 | PASS07 cross-domain interface; authoritative owning master |
| `REQ-SIZE-0006` | `SIZING-OWNED` | `RESEARCH` | `RESEARCH/FUTURE` | SRC-008 lines 6362–6393 | 08 master; deep 06–07 |
| `REQ-DEPLOY-0220` | `CROSS-DOMAIN` | `REJECTED` | `REJECTED` | SRC-008 lines 6690–6725 | CONFLICT_RESOLUTION.md / source history |
