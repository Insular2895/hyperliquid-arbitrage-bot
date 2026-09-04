# Document Target Map

`DOCUMENTATION STATUS: REBUILD IN PROGRESS`

## PASS 02 canonical target overlay

For the 282 requirements reviewed in PASS 02, `06_MARKET_PARTICIPANTS.md` is the Participant master and `deep-specs/participants/01..09` are the detailed targets. Formula-, Data-, Risk-, Execution-, Simulator-, Infrastructure-, Sizing-, Recorder-, Market Atlas- and Validation-owned requirements remain routed to their future owning pass while their Participant interfaces are now covered. The exact row-level mapping and disposition are in `pass02_participants/PARTICIPANT_REQUIREMENT_LEDGER.md`; no requirement ID was renumbered and no PASS 00 row below was globally regenerated.

| Requirement | Status | Master Doc | Deep Spec / destination | Source | Coverage gap |
|---|---|---|---|---|---|
| REQ-BENCH-0001 | RESEARCH | Infrastructure Master | Benchmark Protocol | SRC-001 lines 1–19 | NO |
| REQ-QUANT-0001 | LOCKED | Formula Book | Quant models | SRC-001 lines 20–50 | NO |
| REQ-SEC-0001 | LOCKED | Deployment and Security | Security baseline | SRC-001 lines 51–67 | NO |
| REQ-QUANT-0002 | LOCKED | Formula Book | Quant models | SRC-001 lines 68–87 | NO |
| REQ-CLOCK-0001 | LOCKED | Data Contracts | Clock and RNG contract | SRC-001 lines 88–104 | NO |
| REQ-RISK-0001 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-001 lines 105–126 | NO |
| REQ-EXEC-0001 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-001 lines 127–143 | NO |
| REQ-EXEC-0002 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-001 lines 144–179 | NO |
| REQ-RECOV-0001 | LOCKED | Execution State Machine | Recovery and Unknown State | SRC-001 lines 180–195 | NO |
| REQ-RISK-0002 | SUPERSEDED | Risk Constitution | Risk gates and budgets | SRC-001 lines 196–217 | NO |
| REQ-EXEC-0003 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-001 lines 218–232 | NO |
| REQ-RISK-0003 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-001 lines 233–256 | NO |
| REQ-RISK-0004 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-001 lines 257–278 | NO |
| REQ-GRAPH-0001 | RESEARCH | Market Graph and Routes | Global Graph | SRC-001 lines 279–307 | NO |
| REQ-INFRA-0001 | EXTERNAL_REVALIDATION | Infrastructure Master | Infrastructure deep specs | SRC-001 lines 308–316 | NO |
| REQ-RESEARCH-0001 | LOCKED | Research Appendix | Research candidates | SRC-001 lines 317–356 | NO |
| REQ-VALID-0001 | RESEARCH | Validation Matrix | M0–M5 evidence gates | SRC-001 lines 357–368 | NO |
| REQ-VALID-0002 | FUTURE | Validation Matrix | M0–M5 evidence gates | SRC-001 lines 369–390 | NO |
| REQ-EXEC-0004 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-001 lines 391–416 | NO |
| REQ-REPLAY-0001 | LOCKED | Recorder and Replay | Replay engine | SRC-001 lines 417–438 | NO |
| REQ-REPLAY-0002 | RESEARCH | Recorder and Replay | Replay engine | SRC-001 lines 439–459 | NO |
| REQ-EXEC-0005 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-001 lines 460–479 | NO |
| REQ-EXEC-0006 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-001 lines 480–502 | NO |
| REQ-EXEC-0007 | REJECTED | Execution State Machine | Order/Fill/Cancel contracts | SRC-001 lines 503–534 | NO |
| REQ-OPS-0001 | LOCKED | Operations and Monitoring | Failure/recovery runbooks | SRC-001 lines 535–554 | NO |
| REQ-RECOV-0002 | LOCKED | Execution State Machine | Recovery and Unknown State | SRC-001 lines 555–576 | NO |
| REQ-RECON-0001 | OPEN | Execution State Machine | Reconciliation | SRC-001 lines 577–611 | NO |
| REQ-RISK-0005 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-001 lines 612–623 | NO |
| REQ-RISK-0006 | CALIBRATED | Risk Constitution | Risk gates and budgets | SRC-001 lines 624–641 | NO |
| REQ-BENCH-0002 | RESEARCH | Infrastructure Master | Benchmark Protocol | SRC-001 lines 642–676 | NO |
| REQ-INFRA-0002 | EXTERNAL_REVALIDATION | Infrastructure Master | Infrastructure deep specs | SRC-001 lines 677–696 | NO |
| REQ-ACCT-0001 | CALIBRATED | Accounting | PnL attribution | SRC-001 lines 697–724 | NO |
| REQ-CAP-0001 | FUTURE | Inventory and Capital | Capital reachability/capacity | SRC-001 lines 725–763 | NO |
| REQ-ACCT-0002 | LOCKED | Accounting | PnL attribution | SRC-001 lines 764–786 | NO |
| REQ-RISK-0007 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-001 lines 787–818 | NO |
| REQ-EXEC-0008 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-001 lines 819–963 | NO |
| REQ-VALID-0003 | RESEARCH | Validation Matrix | M0–M5 evidence gates | SRC-001 lines 964–996 | NO |
| REQ-EXEC-0009 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-001 lines 997–1046 | NO |
| REQ-GRAPH-0002 | RESEARCH | Market Graph and Routes | Global Graph | SRC-001 lines 1047–1094 | NO |
| REQ-RISK-0008 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-001 lines 1095–1098 | NO |
| REQ-RISK-0009 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-001 lines 1099–1110 | NO |
| REQ-ARCH-0001 | RESEARCH | Master Architecture | Architecture modules | SRC-001 lines 1111–1126 | NO |
| REQ-BRIDGE-0001 | RESEARCH | Inventory and Capital | Bridge/Relocation | SRC-001 lines 1138–1169 | NO |
| REQ-EXEC-0010 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-001 lines 1170–1207 | NO |
| REQ-RESEARCH-0002 | RESEARCH | Research Appendix | Research candidates | SRC-001 lines 1208–1210 | NO |
| REQ-RESEARCH-0003 | RESEARCH | Research Appendix | Research candidates | SRC-001 lines 1211–1223 | NO |
| REQ-GRAPH-0003 | RESEARCH | Market Graph and Routes | Global Graph | SRC-001 lines 1224–1231 | NO |
| REQ-HWC-0001 | RESEARCH | Master Architecture | Activation policy | SRC-001 lines 1232–1251 | NO |
| REQ-RESEARCH-0004 | RESEARCH | Research Appendix | Research candidates | SRC-001 lines 1252–1275 | NO |
| REQ-HWC-0002 | LOCKED | Master Architecture | Activation policy | SRC-001 lines 1276–1279 | NO |
| REQ-HWC-0003 | RESEARCH | Master Architecture | Activation policy | SRC-001 lines 1280–1281 | NO |
| REQ-ARCH-0002 | RESEARCH | Master Architecture | Architecture modules | SRC-001 lines 1282–1283 | NO |
| REQ-HWC-0004 | RESEARCH | Master Architecture | Activation policy | SRC-001 lines 1284–1292 | NO |
| REQ-INFRA-0003 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-001 lines 1293–1304 | NO |
| REQ-CAP-0002 | RESEARCH | Inventory and Capital | Capital reachability/capacity | SRC-001 lines 1305–1361 | NO |
| REQ-BRIDGE-0002 | LOCKED | Inventory and Capital | Bridge/Relocation | SRC-001 lines 1362–1399 | NO |
| REQ-DATA-0001 | FUTURE | Data Contracts | Schemas and event contracts | SRC-001 lines 1400–1434 | NO |
| REQ-EXEC-0011 | CALIBRATED | Execution State Machine | Order/Fill/Cancel contracts | SRC-001 lines 1435–1454 | NO |
| REQ-ACCT-0003 | LOCKED | Accounting | PnL attribution | SRC-001 lines 1455–1476 | NO |
| REQ-RISK-0010 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-001 lines 1477–1484 | NO |
| REQ-RISK-0011 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-001 lines 1485–1494 | NO |
| REQ-ACCT-0004 | LOCKED | Accounting | PnL attribution | SRC-001 lines 1495–1520 | NO |
| REQ-ARCH-0003 | RESEARCH | Master Architecture | Architecture modules | SRC-001 lines 1521–1524 | NO |
| REQ-EXEC-0012 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-001 lines 1525–1537 | NO |
| REQ-ROUTE-0001 | RESEARCH | Market Graph and Routes | Route/NetConvert contracts | SRC-001 lines 1538–1545 | NO |
| REQ-ACCT-0005 | RESEARCH | Accounting | PnL attribution | SRC-001 lines 1546–1550 | NO |
| REQ-EXEC-0013 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-001 lines 1551–1559 | NO |
| REQ-RECOV-0003 | LOCKED | Execution State Machine | Recovery and Unknown State | SRC-001 lines 1560–1563 | NO |
| REQ-EXEC-0014 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-001 lines 1564–1599 | NO |
| REQ-REPLAY-0003 | RESEARCH | Recorder and Replay | Replay engine | SRC-001 lines 1600–1640 | NO |
| REQ-RESEARCH-0005 | EXTERNAL_REVALIDATION | Research Appendix | Research candidates | SRC-001 lines 1641–1666 | NO |
| REQ-VALID-0004 | RESEARCH | Validation Matrix | M0–M5 evidence gates | SRC-001 lines 1667–1668 | NO |
| REQ-RESEARCH-0006 | RESEARCH | Research Appendix | Research candidates | SRC-001 lines 1669–1670 | NO |
| REQ-VALID-0005 | FUTURE | Validation Matrix | M0–M5 evidence gates | SRC-001 lines 1671–1692 | NO |
| REQ-VALID-0006 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-001 lines 1693–1734 | NO |
| REQ-EXEC-0015 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-001 lines 1735–1769 | NO |
| REQ-VALID-0007 | CALIBRATED | Validation Matrix | M0–M5 evidence gates | SRC-001 lines 1770–1800 | NO |
| REQ-EXEC-0016 | CALIBRATED | Execution State Machine | Order/Fill/Cancel contracts | SRC-001 lines 1801–1824 | NO |
| REQ-DATA-0002 | RESEARCH | Data Contracts | Schemas and event contracts | SRC-001 lines 1825–1844 | NO |
| REQ-BENCH-0003 | RESEARCH | Infrastructure Master | Benchmark Protocol | SRC-001 lines 1845–1874 | NO |
| REQ-GRAPH-0004 | RESEARCH | Market Graph and Routes | Global Graph | SRC-001 lines 1875–1890 | NO |
| REQ-ROUTE-0002 | RESEARCH | Market Graph and Routes | Route/NetConvert contracts | SRC-001 lines 1891–1892 | NO |
| REQ-ARCH-0004 | RESEARCH | Master Architecture | Architecture modules | SRC-001 lines 1893–1894 | NO |
| REQ-BRIDGE-0003 | RESEARCH | Inventory and Capital | Bridge/Relocation | SRC-001 lines 1895–1896 | NO |
| REQ-HWC-0005 | REJECTED | Master Architecture | Activation policy | SRC-001 lines 1897–1900 | NO |
| REQ-GRAPH-0005 | LOCKED | Market Graph and Routes | Global Graph | SRC-001 lines 1901–1928 | NO |
| REQ-EXEC-0017 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-001 lines 1929–2008 | NO |
| REQ-ARCH-0005 | LOCKED | Master Architecture | Architecture modules | SRC-001 lines 2009–2010 | NO |
| REQ-ACCT-0006 | RESEARCH | Accounting | PnL attribution | SRC-001 lines 2011–2012 | NO |
| REQ-INV-0001 | RESEARCH | Inventory and Capital | Inventory Engine | SRC-001 lines 2013–2014 | NO |
| REQ-INFRA-0004 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-001 lines 2015–2027 | NO |
| REQ-GRAPH-0006 | REJECTED | Market Graph and Routes | Global Graph | SRC-001 lines 2028–2056 | NO |
| REQ-EXEC-0018 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-001 lines 2057–2093 | NO |
| REQ-FUTURE-0001 | FUTURE | Future Architecture | Future capability register | SRC-001 lines 2094–2116 | NO |
| REQ-HWC-0006 | RESEARCH | Master Architecture | Activation policy | SRC-001 lines 2117–2129 | NO |
| REQ-ACCT-0007 | RESEARCH | Accounting | PnL attribution | SRC-001 lines 2130–2140 | NO |
| REQ-CAP-0003 | RESEARCH | Inventory and Capital | Capital reachability/capacity | SRC-001 lines 2141–2151 | NO |
| REQ-ARCH-0006 | RESEARCH | Master Architecture | Architecture modules | SRC-001 lines 2152–2159 | NO |
| REQ-ACCT-0008 | REJECTED | Accounting | PnL attribution | SRC-001 lines 2160–2204 | NO |
| REQ-HWC-0007 | RESEARCH | Master Architecture | Activation policy | SRC-001 lines 2205–2268 | NO |
| REQ-ROUTE-0003 | RESEARCH | Market Graph and Routes | Route/NetConvert contracts | SRC-001 lines 2269–2270 | NO |
| REQ-CAP-0004 | LOCKED | Inventory and Capital | Capital reachability/capacity | SRC-001 lines 2271–2291 | NO |
| REQ-INFRA-0005 | CALIBRATED | Infrastructure Master | Infrastructure deep specs | SRC-001 lines 2292–2324 | NO |
| REQ-ACCT-0009 | RESEARCH | Accounting | PnL attribution | SRC-001 lines 2326–2342 | NO |
| REQ-INFRA-0006 | CALIBRATED | Infrastructure Master | Infrastructure deep specs | SRC-001 lines 2343–2360 | NO |
| REQ-EXEC-0019 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-001 lines 2361–2430 | NO |
| REQ-FUTURE-0002 | FUTURE | Future Architecture | Future capability register | SRC-001 lines 2431–2474 | NO |
| REQ-GRAPH-0007 | RESEARCH | Market Graph and Routes | Global Graph | SRC-001 lines 2475–2502 | NO |
| REQ-HWC-0008 | RESEARCH | Master Architecture | Activation policy | SRC-001 lines 2503–2512 | NO |
| REQ-ARCH-0007 | RESEARCH | Master Architecture | Architecture modules | SRC-001 lines 2513–2525 | NO |
| REQ-CAP-0005 | CALIBRATED | Inventory and Capital | Capital reachability/capacity | SRC-001 lines 2526–2577 | NO |
| REQ-EXEC-0020 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-001 lines 2578–2634 | NO |
| REQ-EXEC-0021 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-001 lines 2635–2669 | NO |
| REQ-DEPLOY-0001 | RESEARCH | Deployment and Docker | Client deployment lifecycle | SRC-001 lines 2670–2715 | NO |
| REQ-INFRA-0007 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-001 lines 2716–2754 | NO |
| REQ-ACCT-0010 | RESEARCH | Accounting | PnL attribution | SRC-001 lines 2755–2810 | NO |
| REQ-ROUTE-0004 | RESEARCH | Market Graph and Routes | Route/NetConvert contracts | SRC-001 lines 2811–2843 | NO |
| REQ-ARCH-0008 | CALIBRATED | Master Architecture | Architecture modules | SRC-001 lines 2844–2887 | NO |
| REQ-HWC-0009 | RESEARCH | Master Architecture | Activation policy | SRC-001 lines 2888–2971 | NO |
| REQ-ARCH-0009 | RESEARCH | Master Architecture | Architecture modules | SRC-001 lines 2972–3015 | NO |
| REQ-HWC-0010 | RESEARCH | Master Architecture | Activation policy | SRC-001 lines 3016–3061 | NO |
| REQ-INFRA-0008 | CALIBRATED | Infrastructure Master | Infrastructure deep specs | SRC-001 lines 3062–3126 | NO |
| REQ-INV-0002 | EXTERNAL_REVALIDATION | Inventory and Capital | Inventory Engine | SRC-001 lines 3128–3146 | NO |
| REQ-RISK-0012 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-001 lines 3147–3172 | NO |
| REQ-EXEC-0022 | CALIBRATED | Execution State Machine | Order/Fill/Cancel contracts | SRC-001 lines 3173–3264 | NO |
| REQ-EXEC-0023 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-001 lines 3265–3303 | NO |
| REQ-EXEC-0024 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-001 lines 3304–3337 | NO |
| REQ-ARCH-0010 | RESEARCH | Master Architecture | Architecture modules | SRC-001 lines 3338–3345 | NO |
| REQ-ARCH-0011 | RESEARCH | Master Architecture | Architecture modules | SRC-001 lines 3346–3358 | NO |
| REQ-DATA-0003 | RESEARCH | Data Contracts | Schemas and event contracts | SRC-001 lines 3359–3407 | NO |
| REQ-ATLAS-0001 | RESEARCH | Market Graph and Routes | Market Atlas | SRC-001 lines 3408–3452 | NO |
| REQ-REPLAY-0004 | FUTURE | Recorder and Replay | Replay engine | SRC-001 lines 3453–3492 | NO |
| REQ-CAP-0006 | RESEARCH | Inventory and Capital | Capital reachability/capacity | SRC-001 lines 3493–3550 | NO |
| REQ-DATA-0004 | RESEARCH | Data Contracts | Schemas and event contracts | SRC-001 lines 3551–3555 | NO |
| REQ-HWC-0011 | RESEARCH | Master Architecture | Activation policy | SRC-001 lines 3556–3563 | NO |
| REQ-HWC-0012 | RESEARCH | Master Architecture | Activation policy | SRC-001 lines 3564–3570 | NO |
| REQ-BRIDGE-0004 | RESEARCH | Inventory and Capital | Bridge/Relocation | SRC-001 lines 3571–3577 | NO |
| REQ-CAP-0007 | RESEARCH | Inventory and Capital | Capital reachability/capacity | SRC-001 lines 3578–3584 | NO |
| REQ-ARCH-0012 | RESEARCH | Master Architecture | Architecture modules | SRC-001 lines 3585–3591 | NO |
| REQ-RISK-0013 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-001 lines 3592–3615 | NO |
| REQ-INFRA-0009 | CALIBRATED | Infrastructure Master | Infrastructure deep specs | SRC-001 lines 3616–3658 | NO |
| REQ-VALID-0008 | FUTURE | Validation Matrix | M0–M5 evidence gates | SRC-001 lines 3659–3682 | NO |
| REQ-VALID-0009 | RESEARCH | Validation Matrix | M0–M5 evidence gates | SRC-001 lines 3683–3710 | NO |
| REQ-EXEC-0025 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-001 lines 3711–3830 | NO |
| REQ-FORMULA-0001 | EXTERNAL_REVALIDATION | Formula Book | Formula audit/index | SRC-001 lines 3831–5255 | NO |
| REQ-INFRA-0010 | EXTERNAL_REVALIDATION | Infrastructure Master | Infrastructure deep specs | SRC-002 lines 1–13 | NO |
| REQ-RISK-0014 | FUTURE | Risk Constitution | Risk gates and budgets | SRC-002 lines 14–38 | NO |
| REQ-ARCH-0013 | RESEARCH | Master Architecture | Architecture modules | SRC-002 lines 39–52 | NO |
| REQ-GRAPH-0008 | RESEARCH | Market Graph and Routes | Global Graph | SRC-002 lines 53–64 | NO |
| REQ-ROUTE-0005 | RESEARCH | Market Graph and Routes | Route/NetConvert contracts | SRC-002 lines 65–93 | NO |
| REQ-ROUTE-0006 | RESEARCH | Market Graph and Routes | Route/NetConvert contracts | SRC-002 lines 94–112 | NO |
| REQ-RESEARCH-0007 | RESEARCH | Research Appendix | Research candidates | SRC-002 lines 113–164 | NO |
| REQ-FORMULA-0002 | EXTERNAL_REVALIDATION | Formula Book | Formula audit/index | SRC-002 lines 165–384 | NO |
| REQ-ARCH-0014 | EXTERNAL_REVALIDATION | Master Architecture | Architecture modules | SRC-002 lines 385–405 | NO |
| REQ-ARCH-0015 | LOCKED | Master Architecture | Architecture modules | SRC-002 lines 406–414 | NO |
| REQ-ARCH-0016 | RESEARCH | Master Architecture | Architecture modules | SRC-002 lines 415–417 | NO |
| REQ-MICRO-0001 | RESEARCH | Market Microstructure | OFI/MLOFI/queue | SRC-002 lines 418–427 | NO |
| REQ-EXEC-0026 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 428–436 | NO |
| REQ-INFRA-0011 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-002 lines 437–445 | NO |
| REQ-EXEC-0027 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 446–497 | NO |
| REQ-VALID-0010 | EXTERNAL_REVALIDATION | Validation Matrix | M0–M5 evidence gates | SRC-002 lines 498–506 | NO |
| REQ-PRODUCT-0001 | LOCKED | Product and Scope | Product model | SRC-002 lines 507–804 | NO |
| REQ-EXEC-0028 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 805–845 | NO |
| REQ-MICRO-0002 | LOCKED | Market Microstructure | OFI/MLOFI/queue | SRC-002 lines 846–897 | NO |
| REQ-EXEC-0029 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 898–944 | NO |
| REQ-EXEC-0030 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 945–956 | NO |
| REQ-ARCH-0017 | CALIBRATED | Master Architecture | Architecture modules | SRC-002 lines 957–1019 | NO |
| REQ-FUTURE-0003 | REJECTED | Future Architecture | Future capability register | SRC-002 lines 1020–1082 | NO |
| REQ-EXEC-0031 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 1083–1105 | NO |
| REQ-EXEC-0032 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 1106–1136 | NO |
| REQ-MICRO-0003 | LOCKED | Market Microstructure | OFI/MLOFI/queue | SRC-002 lines 1137–1178 | NO |
| REQ-ARCH-0018 | FUTURE | Master Architecture | Architecture modules | SRC-002 lines 1179–1255 | NO |
| REQ-EXEC-0033 | REJECTED | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 1256–1276 | NO |
| REQ-ARCH-0019 | LOCKED | Master Architecture | Architecture modules | SRC-002 lines 1277–1290 | NO |
| REQ-ACCT-0011 | EXTERNAL_REVALIDATION | Accounting | PnL attribution | SRC-002 lines 1293–1313 | NO |
| REQ-ARCH-0020 | RESEARCH | Master Architecture | Architecture modules | SRC-002 lines 1314–1350 | NO |
| REQ-ARCH-0021 | RESEARCH | Master Architecture | Architecture modules | SRC-002 lines 1351–1352 | NO |
| REQ-INV-0003 | RESEARCH | Inventory and Capital | Inventory Engine | SRC-002 lines 1353–1366 | NO |
| REQ-ARCH-0022 | RESEARCH | Master Architecture | Architecture modules | SRC-002 lines 1367–1368 | NO |
| REQ-EXEC-0034 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 1369–1371 | NO |
| REQ-INV-0004 | EXTERNAL_REVALIDATION | Inventory and Capital | Inventory Engine | SRC-002 lines 1372–1377 | NO |
| REQ-EXEC-0035 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 1378–1405 | NO |
| REQ-RISK-0015 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-002 lines 1406–1439 | NO |
| REQ-EXEC-0036 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 1441–1453 | NO |
| REQ-EXEC-0037 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 1454–1468 | NO |
| REQ-ARCH-0023 | LOCKED | Master Architecture | Architecture modules | SRC-002 lines 1469–1494 | NO |
| REQ-RECOV-0004 | EXTERNAL_REVALIDATION | Execution State Machine | Recovery and Unknown State | SRC-002 lines 1495–1513 | NO |
| REQ-RECOV-0005 | EXTERNAL_REVALIDATION | Execution State Machine | Recovery and Unknown State | SRC-002 lines 1514–1542 | NO |
| REQ-ARCH-0024 | LOCKED | Master Architecture | Architecture modules | SRC-002 lines 1543–1590 | NO |
| REQ-CAP-0008 | RESEARCH | Inventory and Capital | Capital reachability/capacity | SRC-002 lines 1591–1601 | NO |
| REQ-INFRA-0012 | FUTURE | Infrastructure Master | Infrastructure deep specs | SRC-002 lines 1602–1636 | NO |
| REQ-EXEC-0038 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 1637–1664 | NO |
| REQ-CAP-0009 | REJECTED | Inventory and Capital | Capital reachability/capacity | SRC-002 lines 1665–1675 | NO |
| REQ-CAP-0010 | LOCKED | Inventory and Capital | Capital reachability/capacity | SRC-002 lines 1676–1694 | NO |
| REQ-EXEC-0039 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 1695–1726 | NO |
| REQ-GRAPH-0009 | EXTERNAL_REVALIDATION | Market Graph and Routes | Global Graph | SRC-002 lines 1727–1755 | NO |
| REQ-EXEC-0040 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 1756–1792 | NO |
| REQ-ROUTE-0007 | FUTURE | Market Graph and Routes | Route/NetConvert contracts | SRC-002 lines 1793–1818 | NO |
| REQ-ROUTE-0008 | RESEARCH | Market Graph and Routes | Route/NetConvert contracts | SRC-002 lines 1819–1840 | NO |
| REQ-ROUTE-0009 | EXTERNAL_REVALIDATION | Market Graph and Routes | Route/NetConvert contracts | SRC-002 lines 1841–1851 | NO |
| REQ-ACCT-0012 | LOCKED | Accounting | PnL attribution | SRC-002 lines 1852–1866 | NO |
| REQ-ACCT-0013 | RESEARCH | Accounting | PnL attribution | SRC-002 lines 1867–1885 | NO |
| REQ-RECOV-0006 | RESEARCH | Execution State Machine | Recovery and Unknown State | SRC-002 lines 1886–1892 | NO |
| REQ-EXEC-0041 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 1893–1895 | NO |
| REQ-ACCT-0014 | RESEARCH | Accounting | PnL attribution | SRC-002 lines 1896–1902 | NO |
| REQ-ACCT-0015 | RESEARCH | Accounting | PnL attribution | SRC-002 lines 1903–1911 | NO |
| REQ-EXEC-0042 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 1912–1935 | NO |
| REQ-RISK-0016 | FUTURE | Risk Constitution | Risk gates and budgets | SRC-002 lines 1936–1945 | NO |
| REQ-ACCT-0016 | RESEARCH | Accounting | PnL attribution | SRC-002 lines 1946–1958 | NO |
| REQ-ACCT-0017 | LOCKED | Accounting | PnL attribution | SRC-002 lines 1959–1982 | NO |
| REQ-RISK-0017 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-002 lines 1983–1999 | NO |
| REQ-RISK-0018 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-002 lines 2000–2002 | NO |
| REQ-RISK-0019 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-002 lines 2003–2004 | NO |
| REQ-RISK-0020 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-002 lines 2005–2006 | NO |
| REQ-ACCT-0018 | RESEARCH | Accounting | PnL attribution | SRC-002 lines 2007–2009 | NO |
| REQ-RECOV-0007 | RESEARCH | Execution State Machine | Recovery and Unknown State | SRC-002 lines 2010–2034 | NO |
| REQ-ROUTE-0010 | EXTERNAL_REVALIDATION | Market Graph and Routes | Route/NetConvert contracts | SRC-002 lines 2036–2039 | NO |
| REQ-ACCT-0019 | LOCKED | Accounting | PnL attribution | SRC-002 lines 2040–2065 | NO |
| REQ-EXEC-0043 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 2066–2164 | NO |
| REQ-EXEC-0044 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 2165–2193 | NO |
| REQ-EXEC-0045 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 2194–2233 | NO |
| REQ-INFRA-0013 | LOCKED | Infrastructure Master | Infrastructure deep specs | SRC-002 lines 2234–2252 | NO |
| REQ-ROUTE-0011 | RESEARCH | Market Graph and Routes | Route/NetConvert contracts | SRC-002 lines 2253–2283 | NO |
| REQ-ACCT-0020 | EXTERNAL_REVALIDATION | Accounting | PnL attribution | SRC-002 lines 2284–2325 | NO |
| REQ-RESEARCH-0008 | RESEARCH | Research Appendix | Research candidates | SRC-002 lines 2326–2330 | NO |
| REQ-ARCH-0025 | FUTURE | Master Architecture | Architecture modules | SRC-002 lines 2331–2333 | NO |
| REQ-ARCH-0026 | RESEARCH | Master Architecture | Architecture modules | SRC-002 lines 2334–2335 | NO |
| REQ-INV-0005 | RESEARCH | Inventory and Capital | Inventory Engine | SRC-002 lines 2336–2353 | NO |
| REQ-RESEARCH-0009 | LOCKED | Research Appendix | Research candidates | SRC-002 lines 2354–2368 | NO |
| REQ-INV-0006 | EXTERNAL_REVALIDATION | Inventory and Capital | Inventory Engine | SRC-002 lines 2369–2436 | NO |
| REQ-EXEC-0046 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 2437–2449 | NO |
| REQ-HWC-0013 | FUTURE | Master Architecture | Activation policy | SRC-002 lines 2450–2456 | NO |
| REQ-HWC-0014 | RESEARCH | Master Architecture | Activation policy | SRC-002 lines 2457–2462 | NO |
| REQ-HWC-0015 | RESEARCH | Master Architecture | Activation policy | SRC-002 lines 2463–2474 | NO |
| REQ-INFRA-0014 | EXTERNAL_REVALIDATION | Infrastructure Master | Infrastructure deep specs | SRC-002 lines 2475–2511 | NO |
| REQ-GRAPH-0010 | RESEARCH | Market Graph and Routes | Global Graph | SRC-002 lines 2513–2525 | NO |
| REQ-INV-0007 | EXTERNAL_REVALIDATION | Inventory and Capital | Inventory Engine | SRC-002 lines 2526–2527 | NO |
| REQ-ROUTE-0012 | RESEARCH | Market Graph and Routes | Route/NetConvert contracts | SRC-002 lines 2528–2543 | NO |
| REQ-GRAPH-0011 | RESEARCH | Market Graph and Routes | Global Graph | SRC-002 lines 2544–2546 | NO |
| REQ-INFRA-0015 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-002 lines 2547–2582 | NO |
| REQ-CAP-0011 | LOCKED | Inventory and Capital | Capital reachability/capacity | SRC-002 lines 2583–2601 | NO |
| REQ-CAP-0012 | LOCKED | Inventory and Capital | Capital reachability/capacity | SRC-002 lines 2602–2614 | NO |
| REQ-EXEC-0047 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 2615–2656 | NO |
| REQ-FUTURE-0004 | FUTURE | Future Architecture | Future capability register | SRC-002 lines 2657–2673 | NO |
| REQ-QUANT-0003 | LOCKED | Formula Book | Quant models | SRC-002 lines 2674–2704 | NO |
| REQ-CAP-0013 | REJECTED | Inventory and Capital | Capital reachability/capacity | SRC-002 lines 2705–2749 | NO |
| REQ-HWC-0016 | FUTURE | Master Architecture | Activation policy | SRC-002 lines 2750–2798 | NO |
| REQ-RISK-0021 | REJECTED | Risk Constitution | Risk gates and budgets | SRC-002 lines 2799–2815 | NO |
| REQ-CAP-0014 | FUTURE | Inventory and Capital | Capital reachability/capacity | SRC-002 lines 2816–2821 | NO |
| REQ-ARCH-0027 | RESEARCH | Master Architecture | Architecture modules | SRC-002 lines 2822–2824 | NO |
| REQ-TRI-0001 | FUTURE | Market Graph and Routes | Triangle strategy | SRC-002 lines 2825–2844 | NO |
| REQ-ACCT-0021 | LOCKED | Accounting | PnL attribution | SRC-002 lines 2845–2888 | NO |
| REQ-ROUTE-0013 | RESEARCH | Market Graph and Routes | Route/NetConvert contracts | SRC-002 lines 2889–2950 | NO |
| REQ-ACCT-0022 | RESEARCH | Accounting | PnL attribution | SRC-002 lines 2951–2979 | NO |
| REQ-ACCT-0023 | RESEARCH | Accounting | PnL attribution | SRC-002 lines 2980–2990 | NO |
| REQ-ROUTE-0014 | RESEARCH | Market Graph and Routes | Route/NetConvert contracts | SRC-002 lines 2991–2999 | NO |
| REQ-ACCT-0024 | RESEARCH | Accounting | PnL attribution | SRC-002 lines 3000–3008 | NO |
| REQ-ARCH-0028 | RESEARCH | Master Architecture | Architecture modules | SRC-002 lines 3009–3017 | NO |
| REQ-EXEC-0048 | FUTURE | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 3018–3049 | NO |
| REQ-ROUTE-0015 | RESEARCH | Market Graph and Routes | Route/NetConvert contracts | SRC-002 lines 3050–3085 | NO |
| REQ-ARCH-0029 | RESEARCH | Master Architecture | Architecture modules | SRC-002 lines 3086–3090 | NO |
| REQ-ARCH-0030 | RESEARCH | Master Architecture | Architecture modules | SRC-002 lines 3091–3101 | NO |
| REQ-BRIDGE-0005 | RESEARCH | Inventory and Capital | Bridge/Relocation | SRC-002 lines 3102–3126 | NO |
| REQ-RISK-0022 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-002 lines 3127–3151 | NO |
| REQ-HWC-0017 | RESEARCH | Master Architecture | Activation policy | SRC-002 lines 3152–3153 | NO |
| REQ-HWC-0018 | RESEARCH | Master Architecture | Activation policy | SRC-002 lines 3154–3156 | NO |
| REQ-HWC-0019 | RESEARCH | Master Architecture | Activation policy | SRC-002 lines 3157–3165 | NO |
| REQ-HWC-0020 | RESEARCH | Master Architecture | Activation policy | SRC-002 lines 3166–3176 | NO |
| REQ-ACCT-0025 | RESEARCH | Accounting | PnL attribution | SRC-002 lines 3177–3213 | NO |
| REQ-EXEC-0049 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 3214–3251 | NO |
| REQ-INFRA-0016 | LOCKED | Infrastructure Master | Infrastructure deep specs | SRC-002 lines 3252–3274 | NO |
| REQ-ACCT-0026 | FUTURE | Accounting | PnL attribution | SRC-002 lines 3275–3327 | NO |
| REQ-HWC-0021 | RESEARCH | Master Architecture | Activation policy | SRC-002 lines 3328–3334 | NO |
| REQ-HWC-0022 | RESEARCH | Master Architecture | Activation policy | SRC-002 lines 3335–3338 | NO |
| REQ-HWC-0023 | RESEARCH | Master Architecture | Activation policy | SRC-002 lines 3339–3341 | NO |
| REQ-HWC-0024 | RESEARCH | Master Architecture | Activation policy | SRC-002 lines 3342–3358 | NO |
| REQ-RISK-0023 | REJECTED | Risk Constitution | Risk gates and budgets | SRC-002 lines 3359–3380 | NO |
| REQ-ACCT-0027 | LOCKED | Accounting | PnL attribution | SRC-002 lines 3381–3414 | NO |
| REQ-QUANT-0004 | EXTERNAL_REVALIDATION | Formula Book | Quant models | SRC-002 lines 3415–3421 | NO |
| REQ-NODE-0001 | RESEARCH | Infrastructure Master | Node Feed and Scale Gates | SRC-002 lines 3422–3426 | NO |
| REQ-ARCH-0031 | EXTERNAL_REVALIDATION | Master Architecture | Architecture modules | SRC-002 lines 3427–3450 | NO |
| REQ-CLOCK-0002 | RESEARCH | Data Contracts | Clock and RNG contract | SRC-002 lines 3451–3499 | NO |
| REQ-GRAPH-0012 | RESEARCH | Market Graph and Routes | Global Graph | SRC-002 lines 3500–3501 | NO |
| REQ-ARCH-0032 | RESEARCH | Master Architecture | Architecture modules | SRC-002 lines 3502–3504 | NO |
| REQ-INFRA-0017 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-002 lines 3505–3517 | NO |
| REQ-RISK-0024 | FUTURE | Risk Constitution | Risk gates and budgets | SRC-002 lines 3518–3530 | NO |
| REQ-INFRA-0018 | FUTURE | Infrastructure Master | Infrastructure deep specs | SRC-002 lines 3531–3569 | NO |
| REQ-EXEC-0050 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 3570–3603 | NO |
| REQ-ARCH-0033 | RESEARCH | Master Architecture | Architecture modules | SRC-002 lines 3604–3620 | NO |
| REQ-INFRA-0019 | EXTERNAL_REVALIDATION | Infrastructure Master | Infrastructure deep specs | SRC-002 lines 3621–3639 | NO |
| REQ-EXEC-0051 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 3640–3697 | NO |
| REQ-INFRA-0020 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-002 lines 3698–3735 | NO |
| REQ-NODE-0002 | EXTERNAL_REVALIDATION | Infrastructure Master | Node Feed and Scale Gates | SRC-002 lines 3736–3756 | NO |
| REQ-ACCT-0028 | LOCKED | Accounting | PnL attribution | SRC-002 lines 3757–3798 | NO |
| REQ-HWC-0025 | RESEARCH | Master Architecture | Activation policy | SRC-002 lines 3799–3820 | NO |
| REQ-EXEC-0052 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 3821–4351 | NO |
| REQ-ARCH-0034 | RESEARCH | Master Architecture | Architecture modules | SRC-002 lines 4352–4420 | NO |
| REQ-REPLAY-0005 | LOCKED | Recorder and Replay | Replay engine | SRC-002 lines 4421–4478 | NO |
| REQ-ARCH-0035 | CALIBRATED | Master Architecture | Architecture modules | SRC-002 lines 4479–4529 | NO |
| REQ-MICRO-0004 | CALIBRATED | Market Microstructure | OFI/MLOFI/queue | SRC-002 lines 4530–4559 | NO |
| REQ-HWC-0026 | LOCKED | Master Architecture | Activation policy | SRC-002 lines 4560–4619 | NO |
| REQ-ACCT-0029 | RESEARCH | Accounting | PnL attribution | SRC-002 lines 4620–4644 | NO |
| REQ-EXEC-0053 | FUTURE | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 4645–4672 | NO |
| REQ-VALID-0011 | RESEARCH | Validation Matrix | M0–M5 evidence gates | SRC-002 lines 4673–4706 | NO |
| REQ-INFRA-0021 | EXTERNAL_REVALIDATION | Infrastructure Master | Infrastructure deep specs | SRC-002 lines 4707–4726 | NO |
| REQ-INFRA-0022 | EXTERNAL_REVALIDATION | Infrastructure Master | Infrastructure deep specs | SRC-002 lines 4727–4763 | NO |
| REQ-EXEC-0054 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 4764–4846 | NO |
| REQ-ARCH-0036 | FUTURE | Master Architecture | Architecture modules | SRC-002 lines 4847–4868 | NO |
| REQ-VALID-0012 | EXTERNAL_REVALIDATION | Validation Matrix | M0–M5 evidence gates | SRC-002 lines 4869–4874 | NO |
| REQ-EXEC-0055 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 4875–4991 | NO |
| REQ-RISK-0025 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-002 lines 4992–5011 | NO |
| REQ-EXEC-0056 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 5012–5047 | NO |
| REQ-ACCT-0030 | LOCKED | Accounting | PnL attribution | SRC-002 lines 5048–5072 | NO |
| REQ-ARCH-0037 | LOCKED | Master Architecture | Architecture modules | SRC-002 lines 5073–5078 | NO |
| REQ-ROUTE-0016 | RESEARCH | Market Graph and Routes | Route/NetConvert contracts | SRC-002 lines 5079–5100 | NO |
| REQ-ARCH-0038 | RESEARCH | Master Architecture | Architecture modules | SRC-002 lines 5101–5105 | NO |
| REQ-INFRA-0023 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-002 lines 5106–5138 | NO |
| REQ-INFRA-0024 | LOCKED | Infrastructure Master | Infrastructure deep specs | SRC-002 lines 5139–5192 | NO |
| REQ-ARCH-0039 | RESEARCH | Master Architecture | Architecture modules | SRC-002 lines 5193–5220 | NO |
| REQ-BENCH-0004 | LOCKED | Infrastructure Master | Benchmark Protocol | SRC-002 lines 5221–5275 | NO |
| REQ-BRIDGE-0006 | RESEARCH | Inventory and Capital | Bridge/Relocation | SRC-002 lines 5276–5309 | NO |
| REQ-EXEC-0057 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 5310–5392 | NO |
| REQ-RISK-0026 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-002 lines 5393–5428 | NO |
| REQ-INFRA-0025 | LOCKED | Infrastructure Master | Infrastructure deep specs | SRC-002 lines 5429–5450 | NO |
| REQ-INFRA-0026 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-002 lines 5451–5456 | NO |
| REQ-INFRA-0027 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-002 lines 5457–5458 | NO |
| REQ-ARCH-0040 | RESEARCH | Master Architecture | Architecture modules | SRC-002 lines 5459–5460 | NO |
| REQ-INFRA-0028 | FUTURE | Infrastructure Master | Infrastructure deep specs | SRC-002 lines 5461–5465 | NO |
| REQ-INFRA-0029 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-002 lines 5466–5490 | NO |
| REQ-EXEC-0058 | SUPERSEDED | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 5491–5561 | NO |
| REQ-PRODUCT-0002 | RESEARCH | Product and Scope | Product model | SRC-002 lines 5562–5584 | NO |
| REQ-CLOCK-0003 | REJECTED | Data Contracts | Clock and RNG contract | SRC-002 lines 5585–5676 | NO |
| REQ-EXEC-0059 | OPEN | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 5677–5745 | NO |
| REQ-INFRA-0030 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-002 lines 5746–5750 | NO |
| REQ-EXEC-0060 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 5751–5765 | NO |
| REQ-ROUTE-0017 | RESEARCH | Market Graph and Routes | Route/NetConvert contracts | SRC-002 lines 5766–5804 | NO |
| REQ-ROUTE-0018 | FUTURE | Market Graph and Routes | Route/NetConvert contracts | SRC-002 lines 5805–5853 | NO |
| REQ-ARCH-0041 | LOCKED | Master Architecture | Architecture modules | SRC-002 lines 5854–5899 | NO |
| REQ-MICRO-0005 | RESEARCH | Market Microstructure | OFI/MLOFI/queue | SRC-002 lines 5900–5940 | NO |
| REQ-ARCH-0042 | CALIBRATED | Master Architecture | Architecture modules | SRC-002 lines 5941–5973 | NO |
| REQ-ARCH-0043 | LOCKED | Master Architecture | Architecture modules | SRC-002 lines 5974–6016 | NO |
| REQ-RISK-0027 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-002 lines 6017–6051 | NO |
| REQ-EXEC-0061 | REJECTED | Execution State Machine | Order/Fill/Cancel contracts | SRC-002 lines 6052–6077 | NO |
| REQ-EXEC-0062 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 1–30 | NO |
| REQ-EXEC-0063 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 31–51 | NO |
| REQ-ACCT-0031 | CALIBRATED | Accounting | PnL attribution | SRC-003 lines 52–76 | NO |
| REQ-EXEC-0064 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 77–118 | NO |
| REQ-EXEC-0065 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 119–153 | NO |
| REQ-ARCH-0044 | LOCKED | Master Architecture | Architecture modules | SRC-003 lines 154–193 | NO |
| REQ-ROUTE-0019 | REJECTED | Market Graph and Routes | Route/NetConvert contracts | SRC-003 lines 194–201 | NO |
| REQ-EXEC-0066 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 202–218 | NO |
| REQ-REC-0001 | RESEARCH | Recorder and Replay | Recorder/storage contract | SRC-003 lines 219–245 | NO |
| REQ-REC-0002 | RESEARCH | Recorder and Replay | Recorder/storage contract | SRC-003 lines 246–287 | NO |
| REQ-DATA-0005 | RESEARCH | Data Contracts | Schemas and event contracts | SRC-003 lines 288–334 | NO |
| REQ-ACCT-0032 | RESEARCH | Accounting | PnL attribution | SRC-003 lines 335–388 | NO |
| REQ-EXEC-0067 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 389–405 | NO |
| REQ-REPLAY-0006 | EXTERNAL_REVALIDATION | Recorder and Replay | Replay engine | SRC-003 lines 406–426 | NO |
| REQ-REC-0003 | RESEARCH | Recorder and Replay | Recorder/storage contract | SRC-003 lines 427–450 | NO |
| REQ-ARCH-0045 | RESEARCH | Master Architecture | Architecture modules | SRC-003 lines 451–452 | NO |
| REQ-ARCH-0046 | RESEARCH | Master Architecture | Architecture modules | SRC-003 lines 453–454 | NO |
| REQ-DATA-0006 | RESEARCH | Data Contracts | Schemas and event contracts | SRC-003 lines 455–458 | NO |
| REQ-EXEC-0068 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 459–484 | NO |
| REQ-RESEARCH-0010 | RESEARCH | Research Appendix | Research candidates | SRC-003 lines 485–486 | NO |
| REQ-ARCH-0047 | RESEARCH | Master Architecture | Architecture modules | SRC-003 lines 487–488 | NO |
| REQ-ARCH-0048 | RESEARCH | Master Architecture | Architecture modules | SRC-003 lines 489–490 | NO |
| REQ-ARCH-0049 | RESEARCH | Master Architecture | Architecture modules | SRC-003 lines 491–492 | NO |
| REQ-DATA-0007 | RESEARCH | Data Contracts | Schemas and event contracts | SRC-003 lines 493–519 | NO |
| REQ-RISK-0028 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-003 lines 520–568 | NO |
| REQ-DATA-0008 | RESEARCH | Data Contracts | Schemas and event contracts | SRC-003 lines 569–572 | NO |
| REQ-ARCH-0050 | RESEARCH | Master Architecture | Architecture modules | SRC-003 lines 573–579 | NO |
| REQ-ARCH-0051 | RESEARCH | Master Architecture | Architecture modules | SRC-003 lines 580–586 | NO |
| REQ-INFRA-0031 | CALIBRATED | Infrastructure Master | Infrastructure deep specs | SRC-003 lines 587–619 | NO |
| REQ-DATA-0009 | RESEARCH | Data Contracts | Schemas and event contracts | SRC-003 lines 620–634 | NO |
| REQ-PRODUCT-0003 | RESEARCH | Product and Scope | Product model | SRC-003 lines 635–640 | NO |
| REQ-PRODUCT-0004 | RESEARCH | Product and Scope | Product model | SRC-003 lines 641–642 | NO |
| REQ-PRODUCT-0005 | RESEARCH | Product and Scope | Product model | SRC-003 lines 648–672 | NO |
| REQ-PRODUCT-0006 | RESEARCH | Product and Scope | Product model | SRC-003 lines 673–674 | NO |
| REQ-EXEC-0069 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 675–688 | NO |
| REQ-ROUTE-0020 | RESEARCH | Market Graph and Routes | Route/NetConvert contracts | SRC-003 lines 689–700 | NO |
| REQ-INV-0008 | RESEARCH | Inventory and Capital | Inventory Engine | SRC-003 lines 701–711 | NO |
| REQ-ARCH-0052 | RESEARCH | Master Architecture | Architecture modules | SRC-003 lines 712–714 | NO |
| REQ-ARCH-0053 | RESEARCH | Master Architecture | Architecture modules | SRC-003 lines 715–717 | NO |
| REQ-OPS-0002 | RESEARCH | Operations and Monitoring | Failure/recovery runbooks | SRC-003 lines 718–720 | NO |
| REQ-ARCH-0054 | RESEARCH | Master Architecture | Architecture modules | SRC-003 lines 721–752 | NO |
| REQ-PRODUCT-0007 | RESEARCH | Product and Scope | Product model | SRC-003 lines 753–791 | NO |
| REQ-PRODUCT-0008 | RESEARCH | Product and Scope | Product model | SRC-003 lines 792–810 | NO |
| REQ-REC-0004 | RESEARCH | Recorder and Replay | Recorder/storage contract | SRC-003 lines 811–827 | NO |
| REQ-PRODUCT-0009 | RESEARCH | Product and Scope | Product model | SRC-003 lines 828–867 | NO |
| REQ-REC-0005 | RESEARCH | Recorder and Replay | Recorder/storage contract | SRC-003 lines 868–900 | NO |
| REQ-EXEC-0070 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 901–928 | NO |
| REQ-ROUTE-0021 | FUTURE | Market Graph and Routes | Route/NetConvert contracts | SRC-003 lines 929–957 | NO |
| REQ-EXEC-0071 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 958–972 | NO |
| REQ-ARCH-0055 | RESEARCH | Master Architecture | Architecture modules | SRC-003 lines 973–974 | NO |
| REQ-OPS-0003 | RESEARCH | Operations and Monitoring | Failure/recovery runbooks | SRC-003 lines 975–976 | NO |
| REQ-ARCH-0056 | RESEARCH | Master Architecture | Architecture modules | SRC-003 lines 977–978 | NO |
| REQ-ARCH-0057 | RESEARCH | Master Architecture | Architecture modules | SRC-003 lines 979–981 | NO |
| REQ-PRODUCT-0010 | FUTURE | Product and Scope | Product model | SRC-003 lines 982–1027 | NO |
| REQ-ATLAS-0002 | RESEARCH | Market Graph and Routes | Market Atlas | SRC-003 lines 1028–1050 | NO |
| REQ-EXEC-0072 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 1051–1079 | NO |
| REQ-OPS-0004 | CALIBRATED | Operations and Monitoring | Failure/recovery runbooks | SRC-003 lines 1080–1125 | NO |
| REQ-REC-0006 | RESEARCH | Recorder and Replay | Recorder/storage contract | SRC-003 lines 1126–1147 | NO |
| REQ-EXEC-0073 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 1148–1176 | NO |
| REQ-REC-0007 | RESEARCH | Recorder and Replay | Recorder/storage contract | SRC-003 lines 1177–1194 | NO |
| REQ-ARCH-0058 | EXTERNAL_REVALIDATION | Master Architecture | Architecture modules | SRC-003 lines 1195–1196 | NO |
| REQ-ARCH-0059 | RESEARCH | Master Architecture | Architecture modules | SRC-003 lines 1197–1206 | NO |
| REQ-ARCH-0060 | RESEARCH | Master Architecture | Architecture modules | SRC-003 lines 1207–1211 | NO |
| REQ-INFRA-0032 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-003 lines 1212–1245 | NO |
| REQ-ARCH-0061 | RESEARCH | Master Architecture | Architecture modules | SRC-003 lines 1246–1247 | NO |
| REQ-RESEARCH-0011 | RESEARCH | Research Appendix | Research candidates | SRC-003 lines 1248–1250 | NO |
| REQ-PRODUCT-0011 | LOCKED | Product and Scope | Product model | SRC-003 lines 1251–1253 | NO |
| REQ-EXEC-0074 | CALIBRATED | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 1254–1283 | NO |
| REQ-EXEC-0075 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 1284–1338 | NO |
| REQ-HWC-0027 | RESEARCH | Master Architecture | Activation policy | SRC-003 lines 1339–1340 | NO |
| REQ-INFRA-0033 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-003 lines 1341–1356 | NO |
| REQ-EXEC-0076 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 1357–1385 | NO |
| REQ-BRIDGE-0007 | RESEARCH | Inventory and Capital | Bridge/Relocation | SRC-003 lines 1386–1395 | NO |
| REQ-ARCH-0062 | RESEARCH | Master Architecture | Architecture modules | SRC-003 lines 1396–1397 | NO |
| REQ-ARCH-0063 | RESEARCH | Master Architecture | Architecture modules | SRC-003 lines 1398–1399 | NO |
| REQ-RISK-0029 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-003 lines 1400–1412 | NO |
| REQ-RISK-0030 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-003 lines 1413–1428 | NO |
| REQ-EXEC-0077 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 1429–1461 | NO |
| REQ-RISK-0031 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-003 lines 1462–1466 | NO |
| REQ-EXEC-0078 | FUTURE | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 1467–1508 | NO |
| REQ-ARCH-0064 | RESEARCH | Master Architecture | Architecture modules | SRC-003 lines 1509–1534 | NO |
| REQ-RISK-0032 | REJECTED | Risk Constitution | Risk gates and budgets | SRC-003 lines 1535–1562 | NO |
| REQ-EXEC-0079 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 1563–1595 | NO |
| REQ-EXEC-0080 | CALIBRATED | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 1596–1612 | NO |
| REQ-OWA-0001 | EXTERNAL_REVALIDATION | Market Graph and Routes | OWA strategy | SRC-003 lines 1613–1619 | NO |
| REQ-ACCT-0033 | RESEARCH | Accounting | PnL attribution | SRC-003 lines 1620–1697 | NO |
| REQ-EXEC-0081 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 1698–1728 | NO |
| REQ-RESEARCH-0012 | EXTERNAL_REVALIDATION | Research Appendix | Research candidates | SRC-003 lines 1729–1758 | NO |
| REQ-ARCH-0065 | EXTERNAL_REVALIDATION | Master Architecture | Architecture modules | SRC-003 lines 1759–1762 | NO |
| REQ-ARCH-0066 | EXTERNAL_REVALIDATION | Master Architecture | Architecture modules | SRC-003 lines 1763–1772 | NO |
| REQ-ARCH-0067 | RESEARCH | Master Architecture | Architecture modules | SRC-003 lines 1773–1775 | NO |
| REQ-RISK-0033 | EXTERNAL_REVALIDATION | Risk Constitution | Risk gates and budgets | SRC-003 lines 1776–1785 | NO |
| REQ-EXEC-0082 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 1786–1801 | NO |
| REQ-ACCT-0034 | EXTERNAL_REVALIDATION | Accounting | PnL attribution | SRC-003 lines 1802–1819 | NO |
| REQ-ACCT-0035 | LOCKED | Accounting | PnL attribution | SRC-003 lines 1820–1860 | NO |
| REQ-XEX-0001 | EXTERNAL_REVALIDATION | Future Architecture | Cross-exchange future spec | SRC-003 lines 1861–1887 | NO |
| REQ-XEX-0002 | EXTERNAL_REVALIDATION | Future Architecture | Cross-exchange future spec | SRC-003 lines 1888–1894 | NO |
| REQ-EXEC-0083 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 1895–1939 | NO |
| REQ-CAP-0015 | RESEARCH | Inventory and Capital | Capital reachability/capacity | SRC-003 lines 1940–1941 | NO |
| REQ-ARCH-0068 | RESEARCH | Master Architecture | Architecture modules | SRC-003 lines 1942–1947 | NO |
| REQ-RISK-0034 | EXTERNAL_REVALIDATION | Risk Constitution | Risk gates and budgets | SRC-003 lines 1948–1968 | NO |
| REQ-RISK-0035 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-003 lines 1969–1988 | NO |
| REQ-QUANT-0005 | EXTERNAL_REVALIDATION | Formula Book | Quant models | SRC-003 lines 1989–2010 | NO |
| REQ-SEC-0002 | RESEARCH | Deployment and Security | Security baseline | SRC-003 lines 2011–2045 | NO |
| REQ-ARCH-0069 | FUTURE | Master Architecture | Architecture modules | SRC-003 lines 2046–2047 | NO |
| REQ-GRAPH-0013 | FUTURE | Market Graph and Routes | Global Graph | SRC-003 lines 2048–2104 | NO |
| REQ-ACCT-0036 | FUTURE | Accounting | PnL attribution | SRC-003 lines 2105–2120 | NO |
| REQ-RESEARCH-0013 | EXTERNAL_REVALIDATION | Research Appendix | Research candidates | SRC-003 lines 2121–2155 | NO |
| REQ-EXEC-0084 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 2156–2183 | NO |
| REQ-EXEC-0085 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 2184–2214 | NO |
| REQ-OWA-0002 | LOCKED | Market Graph and Routes | OWA strategy | SRC-003 lines 2216–2232 | NO |
| REQ-ACCT-0037 | LOCKED | Accounting | PnL attribution | SRC-003 lines 2233–2252 | NO |
| REQ-ROUTE-0022 | EXTERNAL_REVALIDATION | Market Graph and Routes | Route/NetConvert contracts | SRC-003 lines 2253–2282 | NO |
| REQ-PRODUCT-0012 | RESEARCH | Product and Scope | Product model | SRC-003 lines 2283–2319 | NO |
| REQ-GRAPH-0014 | RESEARCH | Market Graph and Routes | Global Graph | SRC-003 lines 2320–2333 | NO |
| REQ-ROUTE-0023 | RESEARCH | Market Graph and Routes | Route/NetConvert contracts | SRC-003 lines 2334–2354 | NO |
| REQ-ROUTE-0024 | RESEARCH | Market Graph and Routes | Route/NetConvert contracts | SRC-003 lines 2355–2388 | NO |
| REQ-OWA-0003 | RESEARCH | Market Graph and Routes | OWA strategy | SRC-003 lines 2389–2421 | NO |
| REQ-ACCT-0038 | EXTERNAL_REVALIDATION | Accounting | PnL attribution | SRC-003 lines 2422–2443 | NO |
| REQ-BENCH-0005 | LOCKED | Infrastructure Master | Benchmark Protocol | SRC-003 lines 2444–2459 | NO |
| REQ-EXEC-0086 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 2460–2485 | NO |
| REQ-EXEC-0087 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 2486–2510 | NO |
| REQ-EXEC-0088 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 2511–2525 | NO |
| REQ-EXEC-0089 | FUTURE | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 2526–2561 | NO |
| REQ-OWA-0004 | RESEARCH | Market Graph and Routes | OWA strategy | SRC-003 lines 2562–2596 | NO |
| REQ-BRIDGE-0008 | FUTURE | Inventory and Capital | Bridge/Relocation | SRC-003 lines 2597–2615 | NO |
| REQ-ROUTE-0025 | RESEARCH | Market Graph and Routes | Route/NetConvert contracts | SRC-003 lines 2616–2627 | NO |
| REQ-BRIDGE-0009 | FUTURE | Inventory and Capital | Bridge/Relocation | SRC-003 lines 2628–2641 | NO |
| REQ-ACCT-0039 | RESEARCH | Accounting | PnL attribution | SRC-003 lines 2642–2660 | NO |
| REQ-INV-0009 | RESEARCH | Inventory and Capital | Inventory Engine | SRC-003 lines 2661–2674 | NO |
| REQ-INV-0010 | FUTURE | Inventory and Capital | Inventory Engine | SRC-003 lines 2675–2689 | NO |
| REQ-RECOV-0008 | LOCKED | Execution State Machine | Recovery and Unknown State | SRC-003 lines 2690–2709 | NO |
| REQ-ACCT-0040 | RESEARCH | Accounting | PnL attribution | SRC-003 lines 2710–2721 | NO |
| REQ-BRIDGE-0010 | REJECTED | Inventory and Capital | Bridge/Relocation | SRC-003 lines 2722–2750 | NO |
| REQ-EXEC-0090 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 2751–2765 | NO |
| REQ-ACCT-0041 | RESEARCH | Accounting | PnL attribution | SRC-003 lines 2766–2790 | NO |
| REQ-INV-0011 | CALIBRATED | Inventory and Capital | Inventory Engine | SRC-003 lines 2791–2811 | NO |
| REQ-RISK-0036 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-003 lines 2812–2843 | NO |
| REQ-RISK-0037 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-003 lines 2844–2867 | NO |
| REQ-ROUTE-0026 | RESEARCH | Market Graph and Routes | Route/NetConvert contracts | SRC-003 lines 2868–2888 | NO |
| REQ-ACCT-0042 | LOCKED | Accounting | PnL attribution | SRC-003 lines 2889–2905 | NO |
| REQ-RESEARCH-0014 | RESEARCH | Research Appendix | Research candidates | SRC-003 lines 2906–2925 | NO |
| REQ-RECOV-0009 | RESEARCH | Execution State Machine | Recovery and Unknown State | SRC-003 lines 2926–2952 | NO |
| REQ-EXEC-0091 | CALIBRATED | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 2953–2978 | NO |
| REQ-RECOV-0010 | RESEARCH | Execution State Machine | Recovery and Unknown State | SRC-003 lines 2979–2993 | NO |
| REQ-RECOV-0011 | RESEARCH | Execution State Machine | Recovery and Unknown State | SRC-003 lines 2994–3019 | NO |
| REQ-RESEARCH-0015 | RESEARCH | Research Appendix | Research candidates | SRC-003 lines 3020–3023 | NO |
| REQ-EXEC-0092 | REJECTED | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 3024–3046 | NO |
| REQ-SIZE-0001 | RESEARCH | Inventory and Capital | Position Sizing | SRC-003 lines 3047–3070 | NO |
| REQ-RISK-0038 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-003 lines 3071–3083 | NO |
| REQ-SIZE-0002 | EXTERNAL_REVALIDATION | Inventory and Capital | Position Sizing | SRC-003 lines 3084–3100 | NO |
| REQ-RISK-0039 | FUTURE | Risk Constitution | Risk gates and budgets | SRC-003 lines 3101–3119 | NO |
| REQ-SLICE-0001 | RESEARCH | Execution State Machine | Order Slicing | SRC-003 lines 3120–3141 | NO |
| REQ-SLICE-0002 | REJECTED | Execution State Machine | Order Slicing | SRC-003 lines 3142–3161 | NO |
| REQ-CAP-0016 | RESEARCH | Inventory and Capital | Capital reachability/capacity | SRC-003 lines 3162–3187 | NO |
| REQ-INV-0012 | LOCKED | Inventory and Capital | Inventory Engine | SRC-003 lines 3188–3205 | NO |
| REQ-ROUTE-0027 | FUTURE | Market Graph and Routes | Route/NetConvert contracts | SRC-003 lines 3206–3236 | NO |
| REQ-XEX-0003 | RESEARCH | Future Architecture | Cross-exchange future spec | SRC-003 lines 3237–3262 | NO |
| REQ-XEX-0004 | RESEARCH | Future Architecture | Cross-exchange future spec | SRC-003 lines 3263–3291 | NO |
| REQ-ACCT-0043 | RESEARCH | Accounting | PnL attribution | SRC-003 lines 3292–3314 | NO |
| REQ-INV-0013 | FUTURE | Inventory and Capital | Inventory Engine | SRC-003 lines 3315–3330 | NO |
| REQ-VALID-0013 | RESEARCH | Validation Matrix | M0–M5 evidence gates | SRC-003 lines 3331–3345 | NO |
| REQ-VALID-0014 | REJECTED | Validation Matrix | M0–M5 evidence gates | SRC-003 lines 3346–3372 | NO |
| REQ-XEX-0005 | EXTERNAL_REVALIDATION | Future Architecture | Cross-exchange future spec | SRC-003 lines 3373–3393 | NO |
| REQ-XEX-0006 | FUTURE | Future Architecture | Cross-exchange future spec | SRC-003 lines 3394–3420 | NO |
| REQ-ACCT-0044 | RESEARCH | Accounting | PnL attribution | SRC-003 lines 3421–3447 | NO |
| REQ-ACCT-0045 | FUTURE | Accounting | PnL attribution | SRC-003 lines 3448–3464 | NO |
| REQ-EXEC-0093 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 3465–3500 | NO |
| REQ-EXEC-0094 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 3501–3543 | NO |
| REQ-RECOV-0012 | LOCKED | Execution State Machine | Recovery and Unknown State | SRC-003 lines 3544–3566 | NO |
| REQ-RISK-0040 | CALIBRATED | Risk Constitution | Risk gates and budgets | SRC-003 lines 3567–3623 | NO |
| REQ-RECOV-0013 | LOCKED | Execution State Machine | Recovery and Unknown State | SRC-003 lines 3624–3656 | NO |
| REQ-RECOV-0014 | LOCKED | Execution State Machine | Recovery and Unknown State | SRC-003 lines 3657–3691 | NO |
| REQ-EXEC-0095 | FUTURE | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 3692–3759 | NO |
| REQ-ARCH-0070 | RESEARCH | Master Architecture | Architecture modules | SRC-003 lines 3760–3761 | NO |
| REQ-EXEC-0096 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 3762–3797 | NO |
| REQ-RISK-0041 | EXTERNAL_REVALIDATION | Risk Constitution | Risk gates and budgets | SRC-003 lines 3798–3852 | NO |
| REQ-INV-0014 | FUTURE | Inventory and Capital | Inventory Engine | SRC-003 lines 3853–3890 | NO |
| REQ-RISK-0042 | EXTERNAL_REVALIDATION | Risk Constitution | Risk gates and budgets | SRC-003 lines 3891–3928 | NO |
| REQ-INV-0015 | FUTURE | Inventory and Capital | Inventory Engine | SRC-003 lines 3929–3961 | NO |
| REQ-INV-0016 | RESEARCH | Inventory and Capital | Inventory Engine | SRC-003 lines 3962–3971 | NO |
| REQ-RISK-0043 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-003 lines 3972–3980 | NO |
| REQ-INV-0017 | RESEARCH | Inventory and Capital | Inventory Engine | SRC-003 lines 3981–3991 | NO |
| REQ-INV-0018 | RESEARCH | Inventory and Capital | Inventory Engine | SRC-003 lines 3992–4027 | NO |
| REQ-INFRA-0034 | CALIBRATED | Infrastructure Master | Infrastructure deep specs | SRC-003 lines 4028–4054 | NO |
| REQ-ATLAS-0003 | LOCKED | Market Graph and Routes | Market Atlas | SRC-003 lines 4055–4079 | NO |
| REQ-ARCH-0071 | RESEARCH | Master Architecture | Architecture modules | SRC-003 lines 4080–4081 | NO |
| REQ-PRODUCT-0013 | RESEARCH | Product and Scope | Product model | SRC-003 lines 4082–4087 | NO |
| REQ-RISK-0044 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-003 lines 4088–4101 | NO |
| REQ-ARCH-0072 | RESEARCH | Master Architecture | Architecture modules | SRC-003 lines 4102–4103 | NO |
| REQ-INV-0019 | RESEARCH | Inventory and Capital | Inventory Engine | SRC-003 lines 4104–4105 | NO |
| REQ-RECOV-0015 | FUTURE | Execution State Machine | Recovery and Unknown State | SRC-003 lines 4106–4109 | NO |
| REQ-RISK-0045 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-003 lines 4110–4132 | NO |
| REQ-CAP-0017 | RESEARCH | Inventory and Capital | Capital reachability/capacity | SRC-003 lines 4133–4144 | NO |
| REQ-PRODUCT-0014 | RESEARCH | Product and Scope | Product model | SRC-003 lines 4145–4164 | NO |
| REQ-ACCT-0046 | RESEARCH | Accounting | PnL attribution | SRC-003 lines 4165–4189 | NO |
| REQ-ACCT-0047 | RESEARCH | Accounting | PnL attribution | SRC-003 lines 4190–4209 | NO |
| REQ-ACCT-0048 | RESEARCH | Accounting | PnL attribution | SRC-003 lines 4210–4232 | NO |
| REQ-EXEC-0097 | FUTURE | Execution State Machine | Order/Fill/Cancel contracts | SRC-003 lines 4233–4272 | NO |
| REQ-EXEC-0098 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 4–32 | NO |
| REQ-EXEC-0099 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 33–55 | NO |
| REQ-EXEC-0100 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 56–69 | NO |
| REQ-EXEC-0101 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 70–90 | NO |
| REQ-EXEC-0102 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 91–116 | NO |
| REQ-EXEC-0103 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 117–151 | NO |
| REQ-EXEC-0104 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 152–188 | NO |
| REQ-EXEC-0105 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 189–207 | NO |
| REQ-EXEC-0106 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 208–224 | NO |
| REQ-EXEC-0107 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 225–256 | NO |
| REQ-EXEC-0108 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 257–277 | NO |
| REQ-EXEC-0109 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 278–308 | NO |
| REQ-EXEC-0110 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 309–324 | NO |
| REQ-EXEC-0111 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 325–354 | NO |
| REQ-EXEC-0112 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 355–457 | NO |
| REQ-EXEC-0113 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 458–478 | NO |
| REQ-EXEC-0114 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 479–508 | NO |
| REQ-EXEC-0115 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 509–517 | NO |
| REQ-EXEC-0116 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 518–550 | NO |
| REQ-EXEC-0117 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 551–583 | NO |
| REQ-EXEC-0118 | OPEN | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 584–604 | NO |
| REQ-EXEC-0119 | REJECTED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 605–635 | NO |
| REQ-EXEC-0120 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 636–640 | NO |
| REQ-EXEC-0121 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 641–651 | NO |
| REQ-EXEC-0122 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 652–673 | NO |
| REQ-EXEC-0123 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 674–684 | NO |
| REQ-EXEC-0124 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 685–699 | NO |
| REQ-EXEC-0125 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 700–712 | NO |
| REQ-EXEC-0126 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 713–753 | NO |
| REQ-EXEC-0127 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 754–771 | NO |
| REQ-EXEC-0128 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 772–786 | NO |
| REQ-EXEC-0129 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 787–849 | NO |
| REQ-EXEC-0130 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 850–882 | NO |
| REQ-EXEC-0131 | REJECTED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 883–914 | NO |
| REQ-EXEC-0132 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 915–934 | NO |
| REQ-EXEC-0133 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 935–964 | NO |
| REQ-EXEC-0134 | FUTURE | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 965–981 | NO |
| REQ-EXEC-0135 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 982–991 | NO |
| REQ-EXEC-0136 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 992–1013 | NO |
| REQ-EXEC-0137 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1014–1033 | NO |
| REQ-EXEC-0138 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1034–1047 | NO |
| REQ-EXEC-0139 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1048–1063 | NO |
| REQ-EXEC-0140 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1064–1088 | NO |
| REQ-EXEC-0141 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1089–1124 | NO |
| REQ-EXEC-0142 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1125–1138 | NO |
| REQ-EXEC-0143 | FUTURE | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1139–1173 | NO |
| REQ-EXEC-0144 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1174–1185 | NO |
| REQ-EXEC-0145 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1186–1202 | NO |
| REQ-EXEC-0146 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1203–1242 | NO |
| REQ-EXEC-0147 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1243–1264 | NO |
| REQ-EXEC-0148 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1265–1286 | NO |
| REQ-EXEC-0149 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1287–1301 | NO |
| REQ-EXEC-0150 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1302–1320 | NO |
| REQ-EXEC-0151 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1321–1334 | NO |
| REQ-EXEC-0152 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1335–1353 | NO |
| REQ-EXEC-0153 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1354–1370 | NO |
| REQ-EXEC-0154 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1371–1386 | NO |
| REQ-EXEC-0155 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1387–1397 | NO |
| REQ-EXEC-0156 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1398–1417 | NO |
| REQ-EXEC-0157 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1418–1437 | NO |
| REQ-EXEC-0158 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1438–1454 | NO |
| REQ-EXEC-0159 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1455–1480 | NO |
| REQ-EXEC-0160 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1481–1492 | NO |
| REQ-EXEC-0161 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1493–1519 | NO |
| REQ-EXEC-0162 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1520–1535 | NO |
| REQ-EXEC-0163 | FUTURE | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1536–1555 | NO |
| REQ-EXEC-0164 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1556–1578 | NO |
| REQ-EXEC-0165 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1579–1594 | NO |
| REQ-EXEC-0166 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1595–1679 | NO |
| REQ-EXEC-0167 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1680–1692 | NO |
| REQ-EXEC-0168 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1693–1712 | NO |
| REQ-EXEC-0169 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1713–1726 | NO |
| REQ-EXEC-0170 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1727–1747 | NO |
| REQ-EXEC-0171 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1748–1765 | NO |
| REQ-EXEC-0172 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1766–1785 | NO |
| REQ-EXEC-0173 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1786–1798 | NO |
| REQ-EXEC-0174 | OPEN | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1799–1822 | NO |
| REQ-EXEC-0175 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1823–1904 | NO |
| REQ-EXEC-0176 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1905–1927 | NO |
| REQ-EXEC-0177 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1928–1956 | NO |
| REQ-EXEC-0178 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1957–1977 | NO |
| REQ-EXEC-0179 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1978–1997 | NO |
| REQ-EXEC-0180 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 1998–2016 | NO |
| REQ-EXEC-0181 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2017–2038 | NO |
| REQ-EXEC-0182 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2039–2049 | NO |
| REQ-EXEC-0183 | OPEN | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2050–2066 | NO |
| REQ-EXEC-0184 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2067–2075 | NO |
| REQ-EXEC-0185 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2076–2088 | NO |
| REQ-EXEC-0186 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2089–2142 | NO |
| REQ-EXEC-0187 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2143–2207 | NO |
| REQ-EXEC-0188 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2208–2218 | NO |
| REQ-EXEC-0189 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2219–2279 | NO |
| REQ-EXEC-0190 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2280–2300 | NO |
| REQ-EXEC-0191 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2301–2333 | NO |
| REQ-EXEC-0192 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2334–2350 | NO |
| REQ-EXEC-0193 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2351–2374 | NO |
| REQ-EXEC-0194 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2375–2393 | NO |
| REQ-EXEC-0195 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2394–2456 | NO |
| REQ-EXEC-0196 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2457–2475 | NO |
| REQ-EXEC-0197 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2476–2498 | NO |
| REQ-EXEC-0198 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2499–2519 | NO |
| REQ-EXEC-0199 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2520–2532 | NO |
| REQ-EXEC-0200 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2533–2544 | NO |
| REQ-EXEC-0201 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2545–2554 | NO |
| REQ-EXEC-0202 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2555–2577 | NO |
| REQ-EXEC-0203 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2578–2599 | NO |
| REQ-EXEC-0204 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2600–2627 | NO |
| REQ-EXEC-0205 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2628–2651 | NO |
| REQ-EXEC-0206 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2652–2680 | NO |
| REQ-EXEC-0207 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2681–2715 | NO |
| REQ-EXEC-0208 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2716–2730 | NO |
| REQ-EXEC-0209 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2731–2746 | NO |
| REQ-EXEC-0210 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2747–2760 | NO |
| REQ-EXEC-0211 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2761–2773 | NO |
| REQ-EXEC-0212 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2774–2790 | NO |
| REQ-EXEC-0213 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2791–2806 | NO |
| REQ-EXEC-0214 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2807–2814 | NO |
| REQ-EXEC-0215 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2815–2830 | NO |
| REQ-EXEC-0216 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2831–2851 | NO |
| REQ-EXEC-0217 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2852–2869 | NO |
| REQ-EXEC-0218 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2870–2878 | NO |
| REQ-EXEC-0219 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2879–2899 | NO |
| REQ-EXEC-0220 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2900–2918 | NO |
| REQ-EXEC-0221 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2919–2937 | NO |
| REQ-EXEC-0222 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2938–2966 | NO |
| REQ-EXEC-0223 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2967–2986 | NO |
| REQ-EXEC-0224 | FUTURE | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 2987–3002 | NO |
| REQ-EXEC-0225 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 3003–3020 | NO |
| REQ-EXEC-0226 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 3021–3039 | NO |
| REQ-EXEC-0227 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 3040–3052 | NO |
| REQ-EXEC-0228 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 3053–3068 | NO |
| REQ-EXEC-0229 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 3069–3082 | NO |
| REQ-EXEC-0230 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 3083–3105 | NO |
| REQ-EXEC-0231 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 3106–3109 | NO |
| REQ-EXEC-0232 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 3110–3112 | NO |
| REQ-EXEC-0233 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 3113–3115 | NO |
| REQ-EXEC-0234 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 3116–3118 | NO |
| REQ-EXEC-0235 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 3119–3121 | NO |
| REQ-EXEC-0236 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 3122–3134 | NO |
| REQ-EXEC-0237 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 3135–3172 | NO |
| REQ-EXEC-0238 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 3173–3217 | NO |
| REQ-EXEC-0239 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-004 lines 3218–3309 | NO |
| REQ-FORMULA-0003 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 3312–3398 | NO |
| REQ-FORMULA-0004 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 3399–3400 | NO |
| REQ-FORMULA-0005 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 3401–3440 | NO |
| REQ-FORMULA-0006 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 3441–3456 | NO |
| REQ-FORMULA-0007 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 3457–3494 | NO |
| REQ-FORMULA-0008 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 3495–3518 | NO |
| REQ-FORMULA-0009 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 3519–3536 | NO |
| REQ-FORMULA-0010 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 3537–3541 | NO |
| REQ-FORMULA-0011 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 3542–3550 | NO |
| REQ-FORMULA-0012 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 3551–3562 | NO |
| REQ-FORMULA-0013 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 3563–3588 | NO |
| REQ-FORMULA-0014 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 3589–3640 | NO |
| REQ-FORMULA-0015 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 3641–3650 | NO |
| REQ-FORMULA-0016 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 3651–3682 | NO |
| REQ-FORMULA-0017 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 3683–3709 | NO |
| REQ-FORMULA-0018 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 3710–3718 | NO |
| REQ-FORMULA-0019 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 3719–3792 | NO |
| REQ-FORMULA-0020 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 3793–3826 | NO |
| REQ-FORMULA-0021 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 3827–3847 | NO |
| REQ-FORMULA-0022 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 3848–3913 | NO |
| REQ-FORMULA-0023 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 3914–3971 | NO |
| REQ-FORMULA-0024 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 3972–4012 | NO |
| REQ-FORMULA-0025 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 4013–4076 | NO |
| REQ-FORMULA-0026 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 4077–4120 | NO |
| REQ-FORMULA-0027 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 4121–4148 | NO |
| REQ-FORMULA-0028 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 4149–4181 | NO |
| REQ-FORMULA-0029 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 4182–4325 | NO |
| REQ-FORMULA-0030 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 4326–4358 | NO |
| REQ-FORMULA-0031 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 4359–4415 | NO |
| REQ-FORMULA-0032 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 4416–4466 | NO |
| REQ-FORMULA-0033 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 4467–4493 | NO |
| REQ-FORMULA-0034 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 4494–4572 | NO |
| REQ-FORMULA-0035 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 4573–4597 | NO |
| REQ-FORMULA-0036 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 4598–4616 | NO |
| REQ-FORMULA-0037 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 4617–4671 | NO |
| REQ-FORMULA-0038 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 4672–4739 | NO |
| REQ-FORMULA-0039 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 4740–4765 | NO |
| REQ-FORMULA-0040 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 4766–4803 | NO |
| REQ-FORMULA-0041 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 4804–4859 | NO |
| REQ-FORMULA-0042 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 4860–4925 | NO |
| REQ-FORMULA-0043 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 4926–4971 | NO |
| REQ-FORMULA-0044 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 4972–5008 | NO |
| REQ-FORMULA-0045 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 5009–5041 | NO |
| REQ-FORMULA-0046 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 5042–5050 | NO |
| REQ-FORMULA-0047 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 5051–5094 | NO |
| REQ-FORMULA-0048 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 5095–5154 | NO |
| REQ-FORMULA-0049 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 5155–5232 | NO |
| REQ-FORMULA-0050 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 5233–5262 | NO |
| REQ-FORMULA-0051 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 5263–5281 | NO |
| REQ-FORMULA-0052 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 5282–5298 | NO |
| REQ-FORMULA-0053 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 5299–5363 | NO |
| REQ-FORMULA-0054 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 5364–5409 | NO |
| REQ-FORMULA-0055 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 5410–5446 | NO |
| REQ-FORMULA-0056 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 5447–5459 | NO |
| REQ-FORMULA-0057 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 5460–5515 | NO |
| REQ-FORMULA-0058 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 5516–5583 | NO |
| REQ-FORMULA-0059 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 5584–5610 | NO |
| REQ-FORMULA-0060 | LEARNED | Formula Book | Formula audit/index | SRC-004 lines 5611–5674 | NO |
| REQ-FORMULA-0061 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 5675–5693 | NO |
| REQ-FORMULA-0062 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 5694–5726 | NO |
| REQ-FORMULA-0063 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 5727–5784 | NO |
| REQ-FORMULA-0064 | LEARNED | Formula Book | Formula audit/index | SRC-004 lines 5785–5817 | NO |
| REQ-FORMULA-0065 | LEARNED | Formula Book | Formula audit/index | SRC-004 lines 5818–5861 | NO |
| REQ-FORMULA-0066 | LEARNED | Formula Book | Formula audit/index | SRC-004 lines 5862–5889 | NO |
| REQ-FORMULA-0067 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 5890–5925 | NO |
| REQ-FORMULA-0068 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 5926–5971 | NO |
| REQ-FORMULA-0069 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 5972–6021 | NO |
| REQ-FORMULA-0070 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 6022–6054 | NO |
| REQ-FORMULA-0071 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 6055–6081 | NO |
| REQ-FORMULA-0072 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 6082–6149 | NO |
| REQ-FORMULA-0073 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 6150–6245 | NO |
| REQ-FORMULA-0074 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 6246–6282 | NO |
| REQ-FORMULA-0075 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 6283–6313 | NO |
| REQ-FORMULA-0076 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 6314–6342 | NO |
| REQ-FORMULA-0077 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 6343–6391 | NO |
| REQ-FORMULA-0078 | CALIBRATED | Formula Book | Formula audit/index | SRC-004 lines 6392–6491 | NO |
| REQ-FORMULA-0079 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 6492–6517 | NO |
| REQ-FORMULA-0080 | CALIBRATED | Formula Book | Formula audit/index | SRC-004 lines 6518–6542 | NO |
| REQ-FORMULA-0081 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 6543–6589 | NO |
| REQ-FORMULA-0082 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 6590–6622 | NO |
| REQ-FORMULA-0083 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 6623–6692 | NO |
| REQ-FORMULA-0084 | CALIBRATED | Formula Book | Formula audit/index | SRC-004 lines 6693–6763 | NO |
| REQ-FORMULA-0085 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 6764–6820 | NO |
| REQ-FORMULA-0086 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 6821–6886 | NO |
| REQ-FORMULA-0087 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 6887–7003 | NO |
| REQ-FORMULA-0088 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 7004–7078 | NO |
| REQ-FORMULA-0089 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 7079–7140 | NO |
| REQ-FORMULA-0090 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 7141–7273 | NO |
| REQ-FORMULA-0091 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 7274–7313 | NO |
| REQ-FORMULA-0092 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 7314–7342 | NO |
| REQ-FORMULA-0093 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 7343–7380 | NO |
| REQ-FORMULA-0094 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 7381–7468 | NO |
| REQ-FORMULA-0095 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 7469–7546 | NO |
| REQ-FORMULA-0096 | LEARNED | Formula Book | Formula audit/index | SRC-004 lines 7547–7587 | NO |
| REQ-FORMULA-0097 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 7588–7638 | NO |
| REQ-FORMULA-0098 | LEARNED | Formula Book | Formula audit/index | SRC-004 lines 7639–7659 | NO |
| REQ-FORMULA-0099 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 7660–7765 | NO |
| REQ-FORMULA-0100 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 7766–7801 | NO |
| REQ-FORMULA-0101 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 7802–7855 | NO |
| REQ-FORMULA-0102 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 7856–7890 | NO |
| REQ-FORMULA-0103 | LOCKED | Formula Book | Formula audit/index; consumed by Infrastructure Economics | SRC-004 lines 7891–7925 | NO |
| REQ-FORMULA-0104 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 7926–7971 | NO |
| REQ-FORMULA-0105 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 7972–8035 | NO |
| REQ-FORMULA-0106 | CALIBRATED | Formula Book | Formula audit/index | SRC-004 lines 8036–8076 | NO |
| REQ-FORMULA-0107 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 8077–8123 | NO |
| REQ-FORMULA-0108 | LOCKED | Formula Book | Formula audit/index; consumed by Infrastructure Economics | SRC-004 lines 8124–8227 | NO |
| REQ-FORMULA-0109 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 8228–8274 | NO |
| REQ-FORMULA-0110 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 8275–8308 | NO |
| REQ-FORMULA-0111 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 8309–8360 | NO |
| REQ-FORMULA-0112 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 8361–8430 | NO |
| REQ-FORMULA-0113 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 8431–8486 | NO |
| REQ-FORMULA-0114 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 8487–8559 | NO |
| REQ-FORMULA-0115 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 8560–8611 | NO |
| REQ-FORMULA-0116 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 8612–8701 | NO |
| REQ-FORMULA-0117 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 8702–8750 | NO |
| REQ-FORMULA-0118 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 8751–8781 | NO |
| REQ-FORMULA-0119 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 8782–8832 | NO |
| REQ-FORMULA-0120 | CALIBRATED | Formula Book | Formula audit/index | SRC-004 lines 8833–8890 | NO |
| REQ-FORMULA-0121 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 8891–8984 | NO |
| REQ-FORMULA-0122 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 8985–9048 | NO |
| REQ-FORMULA-0123 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 9049–9147 | NO |
| REQ-FORMULA-0124 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 9148–9204 | NO |
| REQ-FORMULA-0125 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 9205–9224 | NO |
| REQ-FORMULA-0126 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 9225–9238 | NO |
| REQ-FORMULA-0127 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 9239–9284 | NO |
| REQ-FORMULA-0128 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 9285–9322 | NO |
| REQ-FORMULA-0129 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 9323–9353 | NO |
| REQ-FORMULA-0130 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 9354–9370 | NO |
| REQ-FORMULA-0131 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 9371–9406 | NO |
| REQ-FORMULA-0132 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 9407–9453 | NO |
| REQ-FORMULA-0133 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 9454–9465 | NO |
| REQ-FORMULA-0134 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 9466–9512 | NO |
| REQ-FORMULA-0135 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 9513–9537 | NO |
| REQ-FORMULA-0136 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 9538–9587 | NO |
| REQ-FORMULA-0137 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 9588–9777 | NO |
| REQ-FORMULA-0138 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 9778–9808 | NO |
| REQ-FORMULA-0139 | LOCKED | Formula Book | Formula audit/index | SRC-004 lines 9809–9953 | NO |
| REQ-RISK-0046 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3–90 | NO |
| REQ-RISK-0047 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 91–145 | NO |
| REQ-RISK-0048 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 147–160 | NO |
| REQ-RISK-0049 | CALIBRATED | Risk Constitution | Risk gates and budgets | SRC-005 lines 161–178 | NO |
| REQ-RISK-0050 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 179–198 | NO |
| REQ-RISK-0051 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 199–221 | NO |
| REQ-RISK-0052 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 222–242 | NO |
| REQ-RISK-0053 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 243–259 | NO |
| REQ-RISK-0054 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 260–328 | NO |
| REQ-RISK-0055 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 329–356 | NO |
| REQ-RISK-0056 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 357–368 | NO |
| REQ-RISK-0057 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 369–380 | NO |
| REQ-RISK-0058 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 381–396 | NO |
| REQ-RISK-0059 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 397–472 | NO |
| REQ-RISK-0060 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 473–485 | NO |
| REQ-RISK-0061 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 486–498 | NO |
| REQ-RISK-0062 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 499–516 | NO |
| REQ-RISK-0063 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 517–565 | NO |
| REQ-RISK-0064 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 566–592 | NO |
| REQ-RISK-0065 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 593–656 | NO |
| REQ-RISK-0066 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 657–673 | NO |
| REQ-RISK-0067 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 674–683 | NO |
| REQ-RISK-0068 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 684–707 | NO |
| REQ-RISK-0069 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 708–717 | NO |
| REQ-RISK-0070 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 718–756 | NO |
| REQ-RISK-0071 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 757–768 | NO |
| REQ-RISK-0072 | FUTURE | Risk Constitution | Risk gates and budgets | SRC-005 lines 769–799 | NO |
| REQ-RISK-0073 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 800–808 | NO |
| REQ-RISK-0074 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 809–836 | NO |
| REQ-RISK-0075 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 837–857 | NO |
| REQ-RISK-0076 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 858–869 | NO |
| REQ-RISK-0077 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 870–883 | NO |
| REQ-RISK-0078 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 884–922 | NO |
| REQ-RISK-0079 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 923–937 | NO |
| REQ-RISK-0080 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 938–951 | NO |
| REQ-RISK-0081 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 952–966 | NO |
| REQ-RISK-0082 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 967–1013 | NO |
| REQ-RISK-0083 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1014–1032 | NO |
| REQ-RISK-0084 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1033–1044 | NO |
| REQ-RISK-0085 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1045–1088 | NO |
| REQ-RISK-0086 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1089–1120 | NO |
| REQ-RISK-0087 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1121–1182 | NO |
| REQ-RISK-0088 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1183–1202 | NO |
| REQ-RISK-0089 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1203–1255 | NO |
| REQ-RISK-0090 | REJECTED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1256–1272 | NO |
| REQ-RISK-0091 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1273–1328 | NO |
| REQ-RISK-0092 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1329–1354 | NO |
| REQ-RISK-0093 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1355–1395 | NO |
| REQ-RISK-0094 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1396–1416 | NO |
| REQ-RISK-0095 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1417–1432 | NO |
| REQ-RISK-0096 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1433–1439 | NO |
| REQ-RISK-0097 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1440–1453 | NO |
| REQ-RISK-0098 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1454–1484 | NO |
| REQ-RISK-0099 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1485–1497 | NO |
| REQ-RISK-0100 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1498–1514 | NO |
| REQ-RISK-0101 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1515–1541 | NO |
| REQ-RISK-0102 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1542–1561 | NO |
| REQ-RISK-0103 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1562–1624 | NO |
| REQ-RISK-0104 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1625–1667 | NO |
| REQ-RISK-0105 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1668–1723 | NO |
| REQ-RISK-0106 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1724–1736 | NO |
| REQ-RISK-0107 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1737–1756 | NO |
| REQ-RISK-0108 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1757–1807 | NO |
| REQ-RISK-0109 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1808–1823 | NO |
| REQ-RISK-0110 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1824–1861 | NO |
| REQ-RISK-0111 | FUTURE | Risk Constitution | Risk gates and budgets | SRC-005 lines 1862–1910 | NO |
| REQ-RISK-0112 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1911–1928 | NO |
| REQ-RISK-0113 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1929–1953 | NO |
| REQ-RISK-0114 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 1954–2027 | NO |
| REQ-RISK-0115 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2028–2077 | NO |
| REQ-RISK-0116 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2078–2090 | NO |
| REQ-RISK-0117 | FUTURE | Risk Constitution | Risk gates and budgets | SRC-005 lines 2091–2111 | NO |
| REQ-RISK-0118 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2112–2141 | NO |
| REQ-RISK-0119 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2142–2155 | NO |
| REQ-RISK-0120 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2156–2171 | NO |
| REQ-RISK-0121 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2172–2182 | NO |
| REQ-RISK-0122 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2183–2199 | NO |
| REQ-RISK-0123 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2200–2243 | NO |
| REQ-RISK-0124 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2244–2289 | NO |
| REQ-RISK-0125 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2290–2326 | NO |
| REQ-RISK-0126 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2327–2341 | NO |
| REQ-RISK-0127 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2342–2357 | NO |
| REQ-RISK-0128 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2358–2378 | NO |
| REQ-RISK-0129 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2379–2414 | NO |
| REQ-RISK-0130 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2415–2427 | NO |
| REQ-RISK-0131 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2428–2457 | NO |
| REQ-RISK-0132 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2458–2484 | NO |
| REQ-RISK-0133 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2485–2512 | NO |
| REQ-RISK-0134 | OPEN | Risk Constitution | Risk gates and budgets | SRC-005 lines 2513–2569 | NO |
| REQ-RISK-0135 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2570–2593 | NO |
| REQ-RISK-0136 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2594–2604 | NO |
| REQ-RISK-0137 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2605–2644 | NO |
| REQ-RISK-0138 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2645–2652 | NO |
| REQ-RISK-0139 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2653–2663 | NO |
| REQ-RISK-0140 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2664–2672 | NO |
| REQ-RISK-0141 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2673–2685 | NO |
| REQ-RISK-0142 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2686–2699 | NO |
| REQ-RISK-0143 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2700–2707 | NO |
| REQ-RISK-0144 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2708–2745 | NO |
| REQ-RISK-0145 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2746–2760 | NO |
| REQ-RISK-0146 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2761–2800 | NO |
| REQ-RISK-0147 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2801–2811 | NO |
| REQ-RISK-0148 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2812–2825 | NO |
| REQ-RISK-0149 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2826–2848 | NO |
| REQ-RISK-0150 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2849–2861 | NO |
| REQ-RISK-0151 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2862–2874 | NO |
| REQ-RISK-0152 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2875–2883 | NO |
| REQ-RISK-0153 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2884–2899 | NO |
| REQ-RISK-0154 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2900–2913 | NO |
| REQ-RISK-0155 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2914–2927 | NO |
| REQ-RISK-0156 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2928–2936 | NO |
| REQ-RISK-0157 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2937–2976 | NO |
| REQ-RISK-0158 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2977–2984 | NO |
| REQ-RISK-0159 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2985–2997 | NO |
| REQ-RISK-0160 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 2999–3003 | NO |
| REQ-RISK-0161 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3004–3014 | NO |
| REQ-RISK-0162 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3015–3020 | NO |
| REQ-RISK-0163 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3021–3027 | NO |
| REQ-RISK-0164 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3028–3043 | NO |
| REQ-RISK-0165 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3044–3058 | NO |
| REQ-RISK-0166 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3059–3070 | NO |
| REQ-RISK-0167 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3071–3084 | NO |
| REQ-RISK-0168 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3085–3088 | NO |
| REQ-RISK-0169 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3089–3100 | NO |
| REQ-RISK-0170 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3101–3110 | NO |
| REQ-RISK-0171 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3111–3123 | NO |
| REQ-RISK-0172 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3124–3136 | NO |
| REQ-RISK-0173 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3137–3145 | NO |
| REQ-RISK-0174 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3146–3166 | NO |
| REQ-RISK-0175 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3167–3179 | NO |
| REQ-RISK-0176 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3180–3199 | NO |
| REQ-RISK-0177 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3200–3209 | NO |
| REQ-RISK-0178 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3210–3224 | NO |
| REQ-RISK-0179 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3225–3237 | NO |
| REQ-RISK-0180 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3238–3247 | NO |
| REQ-RISK-0181 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3248–3260 | NO |
| REQ-RISK-0182 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3261–3272 | NO |
| REQ-RISK-0183 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3273–3281 | NO |
| REQ-RISK-0184 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3282–3290 | NO |
| REQ-RISK-0185 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3291–3300 | NO |
| REQ-RISK-0186 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3301–3317 | NO |
| REQ-RISK-0187 | OPEN | Risk Constitution | Risk gates and budgets | SRC-005 lines 3318–3329 | NO |
| REQ-RISK-0188 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3330–3352 | NO |
| REQ-RISK-0189 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3353–3365 | NO |
| REQ-RISK-0190 | REJECTED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3366–3383 | NO |
| REQ-RISK-0191 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3384–3398 | NO |
| REQ-RISK-0192 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3399–3400 | NO |
| REQ-RISK-0193 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3401–3405 | NO |
| REQ-RISK-0194 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3406–3410 | NO |
| REQ-RISK-0195 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3411–3415 | NO |
| REQ-RISK-0196 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3416–3420 | NO |
| REQ-RISK-0197 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3421–3425 | NO |
| REQ-RISK-0198 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3426–3431 | NO |
| REQ-RISK-0199 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3432–3455 | NO |
| REQ-RISK-0200 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3456–3474 | NO |
| REQ-RISK-0201 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3475–3504 | NO |
| REQ-RISK-0202 | REJECTED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3505–3517 | NO |
| REQ-RISK-0203 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3518–3530 | NO |
| REQ-RISK-0204 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3531–3545 | NO |
| REQ-RISK-0205 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3546–3586 | NO |
| REQ-RISK-0206 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3587–3596 | NO |
| REQ-RISK-0207 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3597–3605 | NO |
| REQ-RISK-0208 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3606–3643 | NO |
| REQ-RISK-0209 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3644–3656 | NO |
| REQ-RISK-0210 | OPEN | Risk Constitution | Risk gates and budgets | SRC-005 lines 3657–3682 | NO |
| REQ-RISK-0211 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3683–3696 | NO |
| REQ-RISK-0212 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3697–3709 | NO |
| REQ-RISK-0213 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3710–3722 | NO |
| REQ-RISK-0214 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3723–3735 | NO |
| REQ-RISK-0215 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3736–3745 | NO |
| REQ-RISK-0216 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3746–3754 | NO |
| REQ-RISK-0217 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3755–3768 | NO |
| REQ-RISK-0218 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3769–3783 | NO |
| REQ-RISK-0219 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3784–3801 | NO |
| REQ-RISK-0220 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3802–3817 | NO |
| REQ-RISK-0221 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3818–3846 | NO |
| REQ-RISK-0222 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3847–3859 | NO |
| REQ-RISK-0223 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3860–3874 | NO |
| REQ-RISK-0224 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3875–3887 | NO |
| REQ-RISK-0225 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3888–3897 | NO |
| REQ-RISK-0226 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3898–3906 | NO |
| REQ-RISK-0227 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3907–3923 | NO |
| REQ-RISK-0228 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3924–3933 | NO |
| REQ-RISK-0229 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3934–3944 | NO |
| REQ-RISK-0230 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3946–3957 | NO |
| REQ-RISK-0231 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3958–3969 | NO |
| REQ-RISK-0232 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3970–3982 | NO |
| REQ-RISK-0233 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3983–3996 | NO |
| REQ-RISK-0234 | CALIBRATED | Risk Constitution | Risk gates and budgets | SRC-005 lines 3997–4007 | NO |
| REQ-RISK-0235 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4008–4020 | NO |
| REQ-RISK-0236 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4021–4034 | NO |
| REQ-RISK-0237 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4035–4047 | NO |
| REQ-RISK-0238 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-005 lines 4048–4062 | NO |
| REQ-RISK-0239 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4063–4075 | NO |
| REQ-RISK-0240 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4076–4089 | NO |
| REQ-RISK-0241 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4090–4102 | NO |
| REQ-RISK-0242 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4103–4112 | NO |
| REQ-RISK-0243 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4113–4147 | NO |
| REQ-RISK-0244 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4148–4177 | NO |
| REQ-RISK-0245 | FUTURE | Risk Constitution | Risk gates and budgets | SRC-005 lines 4178–4211 | NO |
| REQ-RISK-0246 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4212–4225 | NO |
| REQ-RISK-0247 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4226–4257 | NO |
| REQ-RISK-0248 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4258–4267 | NO |
| REQ-RISK-0249 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4268–4277 | NO |
| REQ-RISK-0250 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4278–4287 | NO |
| REQ-RISK-0251 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4288–4295 | NO |
| REQ-RISK-0252 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4296–4307 | NO |
| REQ-RISK-0253 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4308–4316 | NO |
| REQ-RISK-0254 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4317–4330 | NO |
| REQ-RISK-0255 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4331–4338 | NO |
| REQ-RISK-0256 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4339–4355 | NO |
| REQ-RISK-0257 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4356–4395 | NO |
| REQ-RISK-0258 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4396–4428 | NO |
| REQ-RISK-0259 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4429–4442 | NO |
| REQ-RISK-0260 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4443–4458 | NO |
| REQ-RISK-0261 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4459–4472 | NO |
| REQ-RISK-0262 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4473–4484 | NO |
| REQ-RISK-0263 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4485–4498 | NO |
| REQ-RISK-0264 | FUTURE | Risk Constitution | Risk gates and budgets | SRC-005 lines 4499–4509 | NO |
| REQ-RISK-0265 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4510–4523 | NO |
| REQ-RISK-0266 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4524–4594 | NO |
| REQ-RISK-0267 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4595–4609 | NO |
| REQ-RISK-0268 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4610–4627 | NO |
| REQ-RISK-0269 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4628–4651 | NO |
| REQ-RISK-0270 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4652–4674 | NO |
| REQ-RISK-0271 | REJECTED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4675–4685 | NO |
| REQ-RISK-0272 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4686–4695 | NO |
| REQ-RISK-0273 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4696–4709 | NO |
| REQ-RISK-0274 | REJECTED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4710–4721 | NO |
| REQ-RISK-0275 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4722–4734 | NO |
| REQ-RISK-0276 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4735–4746 | NO |
| REQ-RISK-0277 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4747–4761 | NO |
| REQ-RISK-0278 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4762–4814 | NO |
| REQ-RISK-0279 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4815–4876 | NO |
| REQ-RISK-0280 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4877–4894 | NO |
| REQ-RISK-0281 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4895–4904 | NO |
| REQ-RISK-0282 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4905–4923 | NO |
| REQ-RISK-0283 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4924–4941 | NO |
| REQ-RISK-0284 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4942–4958 | NO |
| REQ-RISK-0285 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4959–4970 | NO |
| REQ-RISK-0286 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4971–4980 | NO |
| REQ-RISK-0287 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4981–4990 | NO |
| REQ-RISK-0288 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 4991–5000 | NO |
| REQ-RISK-0289 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 5001–5009 | NO |
| REQ-RISK-0290 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 5010–5029 | NO |
| REQ-RISK-0291 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 5030–5050 | NO |
| REQ-RISK-0292 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 5051–5059 | NO |
| REQ-RISK-0293 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 5060–5068 | NO |
| REQ-RISK-0294 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 5069–5080 | NO |
| REQ-RISK-0295 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 5081–5131 | NO |
| REQ-RISK-0296 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 5132–5185 | NO |
| REQ-RISK-0297 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 5186–5241 | NO |
| REQ-RISK-0298 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-005 lines 5242–5373 | NO |
| REQ-DATA-0010 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5376–5410 | NO |
| REQ-DATA-0011 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5411–5438 | NO |
| REQ-DATA-0012 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5440–5450 | NO |
| REQ-DATA-0013 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5451–5462 | NO |
| REQ-DATA-0014 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5463–5472 | NO |
| REQ-DATA-0015 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5473–5482 | NO |
| REQ-DATA-0016 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5483–5492 | NO |
| REQ-DATA-0017 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5493–5503 | NO |
| REQ-DATA-0018 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5504–5530 | NO |
| REQ-DATA-0019 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5531–5548 | NO |
| REQ-REC-0008 | LOCKED | Recorder and Replay | Recorder/storage contract | SRC-005 lines 5549–5565 | NO |
| REQ-DATA-0020 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5566–5579 | NO |
| REQ-CLOCK-0004 | LOCKED | Data Contracts | Clock and RNG contract | SRC-005 lines 5580–5589 | NO |
| REQ-CLOCK-0005 | LOCKED | Data Contracts | Clock and RNG contract | SRC-005 lines 5590–5599 | NO |
| REQ-DATA-0021 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5600–5613 | NO |
| REQ-DATA-0022 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5614–5625 | NO |
| REQ-DATA-0023 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5626–5639 | NO |
| REQ-DATA-0024 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5640–5660 | NO |
| REQ-DATA-0025 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5661–5676 | NO |
| REQ-DATA-0026 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5677–5692 | NO |
| REQ-DATA-0027 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5693–5706 | NO |
| REQ-DATA-0028 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5707–5729 | NO |
| REQ-DATA-0029 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5730–5744 | NO |
| REQ-DATA-0030 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5745–5752 | NO |
| REQ-DATA-0031 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5753–5759 | NO |
| REQ-DATA-0032 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5760–5779 | NO |
| REQ-DATA-0033 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5780–5787 | NO |
| REQ-DATA-0034 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5788–5810 | NO |
| REQ-DATA-0035 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5811–5848 | NO |
| REQ-DATA-0036 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5849–5862 | NO |
| REQ-DATA-0037 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5863–5870 | NO |
| REQ-DATA-0038 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5871–5878 | NO |
| REQ-DATA-0039 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5879–5891 | NO |
| REQ-DATA-0040 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5892–5912 | NO |
| REQ-DATA-0041 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5913–5937 | NO |
| REQ-DATA-0042 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5938–5952 | NO |
| REQ-DATA-0043 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5953–5990 | NO |
| REQ-DATA-0044 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 5991–6006 | NO |
| REQ-DATA-0045 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6007–6013 | NO |
| REQ-DATA-0046 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6014–6031 | NO |
| REQ-DATA-0047 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6032–6042 | NO |
| REQ-DATA-0048 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6043–6060 | NO |
| REQ-DATA-0049 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6061–6072 | NO |
| REQ-DATA-0050 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6073–6087 | NO |
| REQ-DATA-0051 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6088–6104 | NO |
| REQ-DATA-0052 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6105–6117 | NO |
| REQ-DATA-0053 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6118–6137 | NO |
| REQ-DATA-0054 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6138–6149 | NO |
| REQ-DATA-0055 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6150–6162 | NO |
| REQ-DATA-0056 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6163–6177 | NO |
| REQ-DATA-0057 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6178–6188 | NO |
| REQ-DATA-0058 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6189–6197 | NO |
| REQ-DATA-0059 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6198–6223 | NO |
| REQ-DATA-0060 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6224–6236 | NO |
| REQ-DATA-0061 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6237–6247 | NO |
| REQ-DATA-0062 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6248–6275 | NO |
| REQ-DATA-0063 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6276–6295 | NO |
| REQ-DATA-0064 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6296–6304 | NO |
| REQ-DATA-0065 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6305–6324 | NO |
| REQ-DATA-0066 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6325–6341 | NO |
| REQ-DATA-0067 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6342–6359 | NO |
| REQ-DATA-0068 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6360–6375 | NO |
| REQ-DATA-0069 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6376–6387 | NO |
| REQ-DATA-0070 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6388–6403 | NO |
| REQ-DATA-0071 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6404–6432 | NO |
| REQ-DATA-0072 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6433–6455 | NO |
| REQ-DATA-0073 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6456–6478 | NO |
| REQ-DATA-0074 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6479–6508 | NO |
| REQ-DATA-0075 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6509–6522 | NO |
| REQ-DATA-0076 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6523–6536 | NO |
| REQ-DATA-0077 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6537–6560 | NO |
| REQ-DATA-0078 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6561–6571 | NO |
| REQ-DATA-0079 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6572–6582 | NO |
| REQ-DATA-0080 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6583–6609 | NO |
| REQ-DATA-0081 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6610–6618 | NO |
| REQ-DATA-0082 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6619–6631 | NO |
| REQ-DATA-0083 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6632–6646 | NO |
| REQ-DATA-0084 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6647–6655 | NO |
| REQ-DATA-0085 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6656–6675 | NO |
| REQ-DATA-0086 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6676–6689 | NO |
| REQ-REPLAY-0007 | LOCKED | Recorder and Replay | Replay engine | SRC-005 lines 6690–6708 | NO |
| REQ-DATA-0087 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6709–6726 | NO |
| REQ-DATA-0088 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6727–6739 | NO |
| REQ-DATA-0089 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6740–6751 | NO |
| REQ-DATA-0090 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6752–6764 | NO |
| REQ-DATA-0091 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6765–6781 | NO |
| REQ-DATA-0092 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6782–6794 | NO |
| REQ-DATA-0093 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6795–6810 | NO |
| REQ-DATA-0094 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6811–6826 | NO |
| REQ-DATA-0095 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6827–6842 | NO |
| REQ-DATA-0096 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6843–6857 | NO |
| REQ-DATA-0097 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6858–6881 | NO |
| REQ-DATA-0098 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6882–6889 | NO |
| REQ-DATA-0099 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6890–6902 | NO |
| REQ-DATA-0100 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6903–6918 | NO |
| REQ-DATA-0101 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6919–6932 | NO |
| REQ-DATA-0102 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6933–6959 | NO |
| REQ-DATA-0103 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6960–6971 | NO |
| REQ-DATA-0104 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 6972–6995 | NO |
| REQ-REPLAY-0008 | LOCKED | Recorder and Replay | Replay engine | SRC-005 lines 6996–7034 | NO |
| REQ-DET-0001 | LOCKED | Data Contracts | Determinism and parity | SRC-005 lines 7035–7075 | NO |
| REQ-DATA-0105 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7076–7086 | NO |
| REQ-DET-0002 | LOCKED | Data Contracts | Determinism and parity | SRC-005 lines 7087–7097 | NO |
| REQ-DATA-0106 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7098–7112 | NO |
| REQ-DATA-0107 | RESEARCH | Data Contracts | Schemas and event contracts | SRC-005 lines 7113–7132 | NO |
| REQ-DATA-0108 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7133–7169 | NO |
| REQ-DATA-0109 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7171–7179 | NO |
| REQ-REPLAY-0009 | LOCKED | Recorder and Replay | Replay engine | SRC-005 lines 7180–7184 | NO |
| REQ-DATA-0110 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7185–7188 | NO |
| REQ-DATA-0111 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7189–7191 | NO |
| REQ-CLOCK-0006 | LOCKED | Data Contracts | Clock and RNG contract | SRC-005 lines 7192–7204 | NO |
| REQ-CLOCK-0007 | LOCKED | Data Contracts | Clock and RNG contract | SRC-005 lines 7205–7212 | NO |
| REQ-CLOCK-0008 | LOCKED | Data Contracts | Clock and RNG contract | SRC-005 lines 7213–7222 | NO |
| REQ-CLOCK-0009 | LOCKED | Data Contracts | Clock and RNG contract | SRC-005 lines 7223–7229 | NO |
| REQ-CLOCK-0010 | LOCKED | Data Contracts | Clock and RNG contract | SRC-005 lines 7230–7236 | NO |
| REQ-CLOCK-0011 | LOCKED | Data Contracts | Clock and RNG contract | SRC-005 lines 7237–7240 | NO |
| REQ-DATA-0112 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7241–7251 | NO |
| REQ-DATA-0113 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7252–7261 | NO |
| REQ-DATA-0114 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7262–7269 | NO |
| REQ-DATA-0115 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7270–7281 | NO |
| REQ-DATA-0116 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7282–7294 | NO |
| REQ-DATA-0117 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7295–7308 | NO |
| REQ-DATA-0118 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7309–7323 | NO |
| REQ-DATA-0119 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7324–7333 | NO |
| REQ-DATA-0120 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7334–7353 | NO |
| REQ-DATA-0121 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7354–7372 | NO |
| REQ-DATA-0122 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7373–7380 | NO |
| REQ-DATA-0123 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7381–7393 | NO |
| REQ-DATA-0124 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7394–7404 | NO |
| REQ-REC-0009 | LOCKED | Recorder and Replay | Recorder/storage contract | SRC-005 lines 7405–7419 | NO |
| REQ-REC-0010 | LOCKED | Recorder and Replay | Recorder/storage contract | SRC-005 lines 7420–7436 | NO |
| REQ-DATA-0125 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7437–7450 | NO |
| REQ-DATA-0126 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7451–7460 | NO |
| REQ-DATA-0127 | RESEARCH | Data Contracts | Schemas and event contracts | SRC-005 lines 7461–7470 | NO |
| REQ-DATA-0128 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7471–7490 | NO |
| REQ-DATA-0129 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7491–7500 | NO |
| REQ-DATA-0130 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7501–7515 | NO |
| REQ-DATA-0131 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7516–7528 | NO |
| REQ-DATA-0132 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7529–7537 | NO |
| REQ-DATA-0133 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7538–7546 | NO |
| REQ-DATA-0134 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7547–7567 | NO |
| REQ-DATA-0135 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7568–7580 | NO |
| REQ-DATA-0136 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7581–7589 | NO |
| REQ-DATA-0137 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7590–7602 | NO |
| REQ-DATA-0138 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7603–7615 | NO |
| REQ-DATA-0139 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7616–7633 | NO |
| REQ-DET-0003 | LOCKED | Data Contracts | Determinism and parity | SRC-005 lines 7634–7642 | NO |
| REQ-DET-0004 | LOCKED | Data Contracts | Determinism and parity | SRC-005 lines 7643–7657 | NO |
| REQ-DATA-0140 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7658–7666 | NO |
| REQ-DATA-0141 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7667–7675 | NO |
| REQ-DATA-0142 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7676–7685 | NO |
| REQ-DATA-0143 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7686–7697 | NO |
| REQ-DATA-0144 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7698–7712 | NO |
| REQ-DATA-0145 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7713–7725 | NO |
| REQ-DATA-0146 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7726–7733 | NO |
| REQ-DATA-0147 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7734–7743 | NO |
| REQ-CLOCK-0012 | LOCKED | Data Contracts | Clock and RNG contract | SRC-005 lines 7744–7751 | NO |
| REQ-DATA-0148 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7752–7766 | NO |
| REQ-DATA-0149 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7767–7785 | NO |
| REQ-DATA-0150 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7786–7804 | NO |
| REQ-DATA-0151 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7805–7812 | NO |
| REQ-DATA-0152 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7813–7824 | NO |
| REQ-DATA-0153 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7825–7841 | NO |
| REQ-DATA-0154 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7842–7851 | NO |
| REQ-DATA-0155 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7852–7865 | NO |
| REQ-DATA-0156 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7866–7882 | NO |
| REQ-DATA-0157 | RESEARCH | Data Contracts | Schemas and event contracts | SRC-005 lines 7883–7887 | NO |
| REQ-DATA-0158 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7888–7900 | NO |
| REQ-DATA-0159 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7901–7908 | NO |
| REQ-DATA-0160 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7909–7917 | NO |
| REQ-DATA-0161 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7918–7933 | NO |
| REQ-DATA-0162 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7934–7936 | NO |
| REQ-DATA-0163 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7937–7952 | NO |
| REQ-DATA-0164 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7953–7960 | NO |
| REQ-REPLAY-0010 | LOCKED | Recorder and Replay | Replay engine | SRC-005 lines 7961–7973 | NO |
| REQ-DATA-0165 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7974–7986 | NO |
| REQ-DATA-0166 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 7987–7995 | NO |
| REQ-REPLAY-0011 | FUTURE | Recorder and Replay | Replay engine | SRC-005 lines 7996–8013 | NO |
| REQ-DATA-0167 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8014–8024 | NO |
| REQ-DATA-0168 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8025–8031 | NO |
| REQ-DATA-0169 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8032–8045 | NO |
| REQ-DATA-0170 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8046–8053 | NO |
| REQ-DATA-0171 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8054–8074 | NO |
| REQ-DATA-0172 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8075–8087 | NO |
| REQ-DATA-0173 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8088–8115 | NO |
| REQ-DATA-0174 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8116–8125 | NO |
| REQ-DATA-0175 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8126–8143 | NO |
| REQ-DATA-0176 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8144–8157 | NO |
| REQ-DATA-0177 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8158–8176 | NO |
| REQ-DATA-0178 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8177–8184 | NO |
| REQ-DATA-0179 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8185–8199 | NO |
| REQ-DATA-0180 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8200–8208 | NO |
| REQ-DATA-0181 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8209–8218 | NO |
| REQ-DATA-0182 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8219–8232 | NO |
| REQ-DATA-0183 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8233–8245 | NO |
| REQ-DATA-0184 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8246–8255 | NO |
| REQ-DATA-0185 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8256–8264 | NO |
| REQ-DATA-0186 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8265–8272 | NO |
| REQ-DATA-0187 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8273–8280 | NO |
| REQ-DATA-0188 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8281–8293 | NO |
| REQ-DATA-0189 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8294–8311 | NO |
| REQ-DATA-0190 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8312–8324 | NO |
| REQ-DATA-0191 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8325–8347 | NO |
| REQ-DATA-0192 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8348–8357 | NO |
| REQ-DET-0005 | LOCKED | Data Contracts | Determinism and parity | SRC-005 lines 8358–8367 | NO |
| REQ-DATA-0193 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8368–8380 | NO |
| REQ-DATA-0194 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8381–8393 | NO |
| REQ-DATA-0195 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8394–8396 | NO |
| REQ-DATA-0196 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8397–8399 | NO |
| REQ-DATA-0197 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8400–8402 | NO |
| REQ-DATA-0198 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8403–8413 | NO |
| REQ-DATA-0199 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8414–8422 | NO |
| REQ-DATA-0200 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8423–8430 | NO |
| REQ-DATA-0201 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8431–8434 | NO |
| REQ-REPLAY-0012 | LOCKED | Recorder and Replay | Replay engine | SRC-005 lines 8435–8442 | NO |
| REQ-DATA-0202 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8443–8461 | NO |
| REQ-DATA-0203 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8462–8474 | NO |
| REQ-DATA-0204 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8475–8483 | NO |
| REQ-DATA-0205 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8484–8493 | NO |
| REQ-DATA-0206 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8494–8503 | NO |
| REQ-DATA-0207 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8504–8513 | NO |
| REQ-DATA-0208 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8514–8522 | NO |
| REQ-REPLAY-0013 | LOCKED | Recorder and Replay | Replay engine | SRC-005 lines 8523–8538 | NO |
| REQ-DET-0006 | LOCKED | Data Contracts | Determinism and parity | SRC-005 lines 8539–8547 | NO |
| REQ-DET-0007 | LOCKED | Data Contracts | Determinism and parity | SRC-005 lines 8548–8566 | NO |
| REQ-DATA-0209 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8567–8576 | NO |
| REQ-DATA-0210 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8577–8585 | NO |
| REQ-DATA-0211 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8586–8592 | NO |
| REQ-DATA-0212 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8593–8603 | NO |
| REQ-DATA-0213 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8604–8611 | NO |
| REQ-DATA-0214 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8612–8624 | NO |
| REQ-DATA-0215 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8625–8634 | NO |
| REQ-DATA-0216 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8635–8642 | NO |
| REQ-DATA-0217 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8643–8651 | NO |
| REQ-DATA-0218 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8652–8657 | NO |
| REQ-DATA-0219 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8658–8669 | NO |
| REQ-DATA-0220 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8670–8672 | NO |
| REQ-DATA-0221 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8673–8681 | NO |
| REQ-DATA-0222 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8682–8692 | NO |
| REQ-DATA-0223 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8693–8703 | NO |
| REQ-DATA-0224 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8704–8709 | NO |
| REQ-DATA-0225 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8710–8717 | NO |
| REQ-DATA-0226 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8718–8725 | NO |
| REQ-REC-0011 | LOCKED | Recorder and Replay | Recorder/storage contract | SRC-005 lines 8726–8734 | NO |
| REQ-DATA-0227 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8735–8746 | NO |
| REQ-DATA-0228 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8747–8753 | NO |
| REQ-DATA-0229 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8754–8763 | NO |
| REQ-DATA-0230 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8764–8773 | NO |
| REQ-DATA-0231 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8774–8776 | NO |
| REQ-DATA-0232 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8777–8786 | NO |
| REQ-DATA-0233 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8787–8795 | NO |
| REQ-DATA-0234 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8796–8798 | NO |
| REQ-DATA-0235 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8799–8806 | NO |
| REQ-DATA-0236 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8807–8815 | NO |
| REQ-CLOCK-0013 | LOCKED | Data Contracts | Clock and RNG contract | SRC-005 lines 8816–8826 | NO |
| REQ-DATA-0237 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8827–8842 | NO |
| REQ-DATA-0238 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8843–8852 | NO |
| REQ-DATA-0239 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8853–8867 | NO |
| REQ-DATA-0240 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8868–8875 | NO |
| REQ-DATA-0241 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8876–8898 | NO |
| REQ-DATA-0242 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8899–8908 | NO |
| REQ-DATA-0243 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8909–8916 | NO |
| REQ-DATA-0244 | FUTURE | Data Contracts | Schemas and event contracts | SRC-005 lines 8917–8924 | NO |
| REQ-DATA-0245 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8925–8939 | NO |
| REQ-REPLAY-0014 | LOCKED | Recorder and Replay | Replay engine | SRC-005 lines 8941–8942 | NO |
| REQ-DATA-0246 | RESEARCH | Data Contracts | Schemas and event contracts | SRC-005 lines 8943–8950 | NO |
| REQ-DATA-0247 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8951–8953 | NO |
| REQ-DATA-0248 | CALIBRATED | Data Contracts | Schemas and event contracts | SRC-005 lines 8954–8971 | NO |
| REQ-DATA-0249 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8972–8974 | NO |
| REQ-DATA-0250 | REJECTED | Data Contracts | Schemas and event contracts | SRC-005 lines 8975–8977 | NO |
| REQ-DATA-0251 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8978–8987 | NO |
| REQ-DATA-0252 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8988–8997 | NO |
| REQ-DATA-0253 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 8998–9008 | NO |
| REQ-DATA-0254 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9009–9018 | NO |
| REQ-DATA-0255 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9019–9025 | NO |
| REQ-DATA-0256 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9026–9032 | NO |
| REQ-DATA-0257 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9033–9035 | NO |
| REQ-DATA-0258 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9036–9043 | NO |
| REQ-DATA-0259 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9044–9050 | NO |
| REQ-DATA-0260 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9051–9057 | NO |
| REQ-DATA-0261 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9058–9067 | NO |
| REQ-DATA-0262 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9068–9085 | NO |
| REQ-DATA-0263 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9086–9093 | NO |
| REQ-DATA-0264 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9094–9100 | NO |
| REQ-DATA-0265 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9101–9119 | NO |
| REQ-DATA-0266 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9120–9128 | NO |
| REQ-DATA-0267 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9129–9131 | NO |
| REQ-DET-0008 | LOCKED | Data Contracts | Determinism and parity | SRC-005 lines 9132–9134 | NO |
| REQ-DET-0009 | LOCKED | Data Contracts | Determinism and parity | SRC-005 lines 9135–9142 | NO |
| REQ-DET-0010 | LOCKED | Data Contracts | Determinism and parity | SRC-005 lines 9143–9149 | NO |
| REQ-DATA-0268 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9150–9157 | NO |
| REQ-DET-0011 | LOCKED | Data Contracts | Determinism and parity | SRC-005 lines 9158–9160 | NO |
| REQ-DET-0012 | LOCKED | Data Contracts | Determinism and parity | SRC-005 lines 9161–9168 | NO |
| REQ-DATA-0269 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9169–9176 | NO |
| REQ-DATA-0270 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9177–9185 | NO |
| REQ-DATA-0271 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9186–9193 | NO |
| REQ-REPLAY-0015 | LOCKED | Recorder and Replay | Replay engine | SRC-005 lines 9194–9201 | NO |
| REQ-REPLAY-0016 | LOCKED | Recorder and Replay | Replay engine | SRC-005 lines 9202–9209 | NO |
| REQ-DATA-0272 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9210–9217 | NO |
| REQ-DATA-0273 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9218–9227 | NO |
| REQ-DATA-0274 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9228–9236 | NO |
| REQ-DATA-0275 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9237–9247 | NO |
| REQ-DATA-0276 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9248–9256 | NO |
| REQ-DATA-0277 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9257–9266 | NO |
| REQ-DATA-0278 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9267–9278 | NO |
| REQ-DATA-0279 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9279–9290 | NO |
| REQ-DATA-0280 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9291–9298 | NO |
| REQ-DATA-0281 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9299–9306 | NO |
| REQ-DATA-0282 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9307–9322 | NO |
| REQ-DATA-0283 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9323–9330 | NO |
| REQ-DET-0013 | RESEARCH | Data Contracts | Determinism and parity | SRC-005 lines 9331–9341 | NO |
| REQ-DATA-0284 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9342–9349 | NO |
| REQ-DET-0014 | LOCKED | Data Contracts | Determinism and parity | SRC-005 lines 9350–9358 | NO |
| REQ-DATA-0285 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9359–9368 | NO |
| REQ-DATA-0286 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9369–9375 | NO |
| REQ-DATA-0287 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9376–9378 | NO |
| REQ-DATA-0288 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9379–9381 | NO |
| REQ-DATA-0289 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9382–9390 | NO |
| REQ-DATA-0290 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9391–9393 | NO |
| REQ-DATA-0291 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9394–9402 | NO |
| REQ-DATA-0292 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9403–9413 | NO |
| REQ-DATA-0293 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9414–9423 | NO |
| REQ-DATA-0294 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9424–9435 | NO |
| REQ-DATA-0295 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9436–9446 | NO |
| REQ-DATA-0296 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9447–9456 | NO |
| REQ-DATA-0297 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9457–9467 | NO |
| REQ-DATA-0298 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9468–9484 | NO |
| REQ-DATA-0299 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9485–9504 | NO |
| REQ-DATA-0300 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9505–9512 | NO |
| REQ-DATA-0301 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9513–9539 | NO |
| REQ-DATA-0302 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9540–9549 | NO |
| REQ-DATA-0303 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9550–9558 | NO |
| REQ-DATA-0304 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9559–9567 | NO |
| REQ-DATA-0305 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9568–9570 | NO |
| REQ-DATA-0306 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9571–9579 | NO |
| REQ-DATA-0307 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9580–9582 | NO |
| REQ-DATA-0308 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9583–9585 | NO |
| REQ-DET-0015 | LOCKED | Data Contracts | Determinism and parity | SRC-005 lines 9586–9669 | NO |
| REQ-DATA-0309 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9670–9680 | NO |
| REQ-DATA-0310 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9681–9692 | NO |
| REQ-REPLAY-0017 | LOCKED | Recorder and Replay | Replay engine | SRC-005 lines 9693–9702 | NO |
| REQ-DATA-0311 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9703–9710 | NO |
| REQ-DATA-0312 | CALIBRATED | Data Contracts | Schemas and event contracts | SRC-005 lines 9711–9718 | NO |
| REQ-DATA-0313 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9719–9744 | NO |
| REQ-DATA-0314 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9745–9779 | NO |
| REQ-DATA-0315 | LOCKED | Data Contracts | Schemas and event contracts | SRC-005 lines 9780–9877 | NO |
| REQ-DEPLOY-0002 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 5–40 | NO |
| REQ-DEPLOY-0003 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 41–76 | NO |
| REQ-CLIENT-0001 | LOCKED | Product and Deployment | Client distribution model | SRC-006 lines 77–111 | NO |
| REQ-DEPLOY-0004 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 112–147 | NO |
| REQ-DEPLOY-0005 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 148–175 | NO |
| REQ-DEPLOY-0006 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 176–189 | NO |
| REQ-DEPLOY-0007 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 190–207 | NO |
| REQ-DEPLOY-0008 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 208–226 | NO |
| REQ-DEPLOY-0009 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 227–240 | NO |
| REQ-DEPLOY-0010 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 241–260 | NO |
| REQ-DEPLOY-0011 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 261–278 | NO |
| REQ-DEPLOY-0012 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 279–293 | NO |
| REQ-DEPLOY-0013 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 294–322 | NO |
| REQ-DEPLOY-0014 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 323–341 | NO |
| REQ-DEPLOY-0015 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 342–351 | NO |
| REQ-DEPLOY-0016 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 352–361 | NO |
| REQ-DEPLOY-0017 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 362–378 | NO |
| REQ-DEPLOY-0018 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 379–393 | NO |
| REQ-DEPLOY-0019 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 394–411 | NO |
| REQ-DEPLOY-0020 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 412–420 | NO |
| REQ-DEPLOY-0021 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 421–437 | NO |
| REQ-DEPLOY-0022 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 438–452 | NO |
| REQ-DEPLOY-0023 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 453–461 | NO |
| REQ-SEC-0003 | LOCKED | Deployment and Security | Security baseline | SRC-006 lines 462–471 | NO |
| REQ-SEC-0004 | LOCKED | Deployment and Security | Security baseline | SRC-006 lines 472–487 | NO |
| REQ-DEPLOY-0024 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 488–496 | NO |
| REQ-DEPLOY-0025 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 497–510 | NO |
| REQ-DEPLOY-0026 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 511–519 | NO |
| REQ-DEPLOY-0027 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 520–536 | NO |
| REQ-DEPLOY-0028 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 537–550 | NO |
| REQ-SEC-0005 | LOCKED | Deployment and Security | Security baseline | SRC-006 lines 551–559 | NO |
| REQ-DEPLOY-0029 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 560–568 | NO |
| REQ-DEPLOY-0030 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 569–577 | NO |
| REQ-DEPLOY-0031 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 578–585 | NO |
| REQ-DEPLOY-0032 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 586–599 | NO |
| REQ-OPS-0005 | LOCKED | Operations and Monitoring | Failure/recovery runbooks | SRC-006 lines 600–603 | NO |
| REQ-DEPLOY-0033 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 604–615 | NO |
| REQ-DEPLOY-0034 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 616–626 | NO |
| REQ-DEPLOY-0035 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 627–651 | NO |
| REQ-DEPLOY-0036 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 652–680 | NO |
| REQ-DEPLOY-0037 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 681–689 | NO |
| REQ-DEPLOY-0038 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 690–702 | NO |
| REQ-DEPLOY-0039 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 703–711 | NO |
| REQ-DEPLOY-0040 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 712–721 | NO |
| REQ-DEPLOY-0041 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 722–740 | NO |
| REQ-DEPLOY-0042 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 741–748 | NO |
| REQ-DEPLOY-0043 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 749–761 | NO |
| REQ-DEPLOY-0044 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 762–769 | NO |
| REQ-DEPLOY-0045 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 770–781 | NO |
| REQ-DEPLOY-0046 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 782–792 | NO |
| REQ-DEPLOY-0047 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 793–801 | NO |
| REQ-DEPLOY-0048 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 802–820 | NO |
| REQ-DEPLOY-0049 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 821–834 | NO |
| REQ-DEPLOY-0050 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 835–841 | NO |
| REQ-DEPLOY-0051 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 842–854 | NO |
| REQ-SEC-0006 | LOCKED | Deployment and Security | Security baseline | SRC-006 lines 855–861 | NO |
| REQ-SEC-0007 | LOCKED | Deployment and Security | Security baseline | SRC-006 lines 862–869 | NO |
| REQ-SEC-0008 | LOCKED | Deployment and Security | Security baseline | SRC-006 lines 870–882 | NO |
| REQ-DEPLOY-0052 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 883–897 | NO |
| REQ-SEC-0009 | LOCKED | Deployment and Security | Security baseline | SRC-006 lines 898–906 | NO |
| REQ-SEC-0010 | LOCKED | Deployment and Security | Security baseline | SRC-006 lines 907–917 | NO |
| REQ-DEPLOY-0053 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 918–925 | NO |
| REQ-SEC-0011 | LOCKED | Deployment and Security | Security baseline | SRC-006 lines 926–933 | NO |
| REQ-DEPLOY-0054 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 934–940 | NO |
| REQ-CLIENT-0002 | LOCKED | Product and Deployment | Client distribution model | SRC-006 lines 941–956 | NO |
| REQ-CLIENT-0003 | LOCKED | Product and Deployment | Client distribution model | SRC-006 lines 957–969 | NO |
| REQ-DEPLOY-0055 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 970–972 | NO |
| REQ-DEPLOY-0056 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 973–983 | NO |
| REQ-DEPLOY-0057 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 984–992 | NO |
| REQ-DEPLOY-0058 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 993–1000 | NO |
| REQ-DEPLOY-0059 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1001–1008 | NO |
| REQ-DEPLOY-0060 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1009–1017 | NO |
| REQ-DEPLOY-0061 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1018–1019 | NO |
| REQ-DEPLOY-0062 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1020–1026 | NO |
| REQ-DEPLOY-0063 | CALIBRATED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1027–1034 | NO |
| REQ-DEPLOY-0064 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1035–1044 | NO |
| REQ-DEPLOY-0065 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1045–1048 | NO |
| REQ-DEPLOY-0066 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1049–1057 | NO |
| REQ-DEPLOY-0067 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1058–1073 | NO |
| REQ-DEPLOY-0068 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1074–1082 | NO |
| REQ-DEPLOY-0069 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1083–1091 | NO |
| REQ-DEPLOY-0070 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1092–1099 | NO |
| REQ-DEPLOY-0071 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1100–1109 | NO |
| REQ-DEPLOY-0072 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1110–1119 | NO |
| REQ-DEPLOY-0073 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1120–1130 | NO |
| REQ-DEPLOY-0074 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1131–1133 | NO |
| REQ-OPS-0006 | LOCKED | Operations and Monitoring | Failure/recovery runbooks | SRC-006 lines 1134–1143 | NO |
| REQ-DEPLOY-0075 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1144–1146 | NO |
| REQ-SEC-0012 | LOCKED | Deployment and Security | Security baseline | SRC-006 lines 1147–1155 | NO |
| REQ-DEPLOY-0076 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1156–1166 | NO |
| REQ-OPS-0007 | LOCKED | Operations and Monitoring | Failure/recovery runbooks | SRC-006 lines 1167–1174 | NO |
| REQ-OPS-0008 | LOCKED | Operations and Monitoring | Failure/recovery runbooks | SRC-006 lines 1175–1187 | NO |
| REQ-DEPLOY-0077 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1188–1198 | NO |
| REQ-DEPLOY-0078 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1199–1206 | NO |
| REQ-OPS-0009 | LOCKED | Operations and Monitoring | Failure/recovery runbooks | SRC-006 lines 1207–1215 | NO |
| REQ-OPS-0010 | LOCKED | Operations and Monitoring | Failure/recovery runbooks | SRC-006 lines 1216–1228 | NO |
| REQ-OPS-0011 | LOCKED | Operations and Monitoring | Failure/recovery runbooks | SRC-006 lines 1229–1238 | NO |
| REQ-DEPLOY-0079 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1239–1247 | NO |
| REQ-OPS-0012 | LOCKED | Operations and Monitoring | Failure/recovery runbooks | SRC-006 lines 1248–1251 | NO |
| REQ-DEPLOY-0080 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1252–1259 | NO |
| REQ-DEPLOY-0081 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1260–1268 | NO |
| REQ-DEPLOY-0082 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1269–1284 | NO |
| REQ-DEPLOY-0083 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1285–1292 | NO |
| REQ-DEPLOY-0084 | OPEN | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1293–1306 | NO |
| REQ-SEC-0013 | LOCKED | Deployment and Security | Security baseline | SRC-006 lines 1307–1315 | NO |
| REQ-DEPLOY-0085 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1316–1325 | NO |
| REQ-CLIENT-0004 | LOCKED | Product and Deployment | Client distribution model | SRC-006 lines 1326–1335 | NO |
| REQ-DEPLOY-0086 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1336–1347 | NO |
| REQ-DEPLOY-0087 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1348–1366 | NO |
| REQ-DEPLOY-0088 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1367–1375 | NO |
| REQ-DEPLOY-0089 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1376–1382 | NO |
| REQ-DEPLOY-0090 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1383–1395 | NO |
| REQ-CLIENT-0005 | LOCKED | Product and Deployment | Client distribution model | SRC-006 lines 1396–1410 | NO |
| REQ-CLIENT-0006 | LOCKED | Product and Deployment | Client distribution model | SRC-006 lines 1411–1421 | NO |
| REQ-DEPLOY-0091 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1422–1428 | NO |
| REQ-DEPLOY-0092 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1429–1441 | NO |
| REQ-DEPLOY-0093 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1442–1456 | NO |
| REQ-DEPLOY-0094 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1457–1477 | NO |
| REQ-DEPLOY-0095 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1478–1489 | NO |
| REQ-DEPLOY-0096 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1490–1498 | NO |
| REQ-DEPLOY-0097 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1499–1509 | NO |
| REQ-DEPLOY-0098 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1510–1519 | NO |
| REQ-DEPLOY-0099 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1520–1529 | NO |
| REQ-DEPLOY-0100 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1530–1540 | NO |
| REQ-CLIENT-0007 | LOCKED | Product and Deployment | Client distribution model | SRC-006 lines 1541–1557 | NO |
| REQ-DEPLOY-0101 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1558–1561 | NO |
| REQ-CLIENT-0008 | LOCKED | Product and Deployment | Client distribution model | SRC-006 lines 1562–1573 | NO |
| REQ-LIC-0001 | LOCKED | Deployment and Security | License contract | SRC-006 lines 1574–1581 | NO |
| REQ-DEPLOY-0102 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1582–1588 | NO |
| REQ-DEPLOY-0103 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1589–1596 | NO |
| REQ-LIC-0002 | LOCKED | Deployment and Security | License contract | SRC-006 lines 1597–1608 | NO |
| REQ-LIC-0003 | LOCKED | Deployment and Security | License contract | SRC-006 lines 1609–1619 | NO |
| REQ-DEPLOY-0104 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1620–1627 | NO |
| REQ-DEPLOY-0105 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1628–1635 | NO |
| REQ-DEPLOY-0106 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1636–1646 | NO |
| REQ-DEPLOY-0107 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1647–1658 | NO |
| REQ-DEPLOY-0108 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1659–1666 | NO |
| REQ-DEPLOY-0109 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1667–1679 | NO |
| REQ-DEPLOY-0110 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1680–1687 | NO |
| REQ-DEPLOY-0111 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1688–1697 | NO |
| REQ-LIC-0004 | LOCKED | Deployment and Security | License contract | SRC-006 lines 1698–1704 | NO |
| REQ-DEPLOY-0112 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1705–1712 | NO |
| REQ-DEPLOY-0113 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1713–1722 | NO |
| REQ-DEPLOY-0114 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1723–1732 | NO |
| REQ-DEPLOY-0115 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1733–1741 | NO |
| REQ-DEPLOY-0116 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1742–1744 | NO |
| REQ-DEPLOY-0117 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1745–1747 | NO |
| REQ-DEPLOY-0118 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1748–1750 | NO |
| REQ-DEPLOY-0119 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1751–1774 | NO |
| REQ-CLIENT-0009 | LOCKED | Product and Deployment | Client distribution model | SRC-006 lines 1775–1777 | NO |
| REQ-DEPLOY-0120 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1778–1788 | NO |
| REQ-CLIENT-0010 | LOCKED | Product and Deployment | Client distribution model | SRC-006 lines 1789–1796 | NO |
| REQ-DEPLOY-0121 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1797–1815 | NO |
| REQ-DEPLOY-0122 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1816–1832 | NO |
| REQ-DEPLOY-0123 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1833–1844 | NO |
| REQ-DEPLOY-0124 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1845–1854 | NO |
| REQ-DEPLOY-0125 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1855–1870 | NO |
| REQ-DEPLOY-0126 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1871–1877 | NO |
| REQ-DEPLOY-0127 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1878–1888 | NO |
| REQ-DEPLOY-0128 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1889–1892 | NO |
| REQ-DEPLOY-0129 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1893–1905 | NO |
| REQ-DEPLOY-0130 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1906–1914 | NO |
| REQ-DEPLOY-0131 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1915–1917 | NO |
| REQ-DEPLOY-0132 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1918–1927 | NO |
| REQ-DEPLOY-0133 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1928–1938 | NO |
| REQ-DEPLOY-0134 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1939–1945 | NO |
| REQ-DEPLOY-0135 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1946–1953 | NO |
| REQ-DEPLOY-0136 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1954–1962 | NO |
| REQ-DEPLOY-0137 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1963–1965 | NO |
| REQ-DEPLOY-0138 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1966–1968 | NO |
| REQ-DEPLOY-0139 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1969–1980 | NO |
| REQ-DEPLOY-0140 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 1981–1987 | NO |
| REQ-OPS-0013 | LOCKED | Operations and Monitoring | Failure/recovery runbooks | SRC-006 lines 1988–1995 | NO |
| REQ-OPS-0014 | LOCKED | Operations and Monitoring | Failure/recovery runbooks | SRC-006 lines 1996–2009 | NO |
| REQ-DEPLOY-0141 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2010–2017 | NO |
| REQ-DEPLOY-0142 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2018–2020 | NO |
| REQ-DEPLOY-0143 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2021–2029 | NO |
| REQ-DEPLOY-0144 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2030–2043 | NO |
| REQ-DEPLOY-0145 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2044–2047 | NO |
| REQ-DEPLOY-0146 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2048–2062 | NO |
| REQ-DEPLOY-0147 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2063–2073 | NO |
| REQ-DEPLOY-0148 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2074–2085 | NO |
| REQ-DEPLOY-0149 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2086–2101 | NO |
| REQ-DEPLOY-0150 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2102–2110 | NO |
| REQ-DEPLOY-0151 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2111–2118 | NO |
| REQ-DEPLOY-0152 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2119–2126 | NO |
| REQ-DEPLOY-0153 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2127–2134 | NO |
| REQ-CLIENT-0011 | LOCKED | Product and Deployment | Client distribution model | SRC-006 lines 2135–2144 | NO |
| REQ-DEPLOY-0154 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2145–2154 | NO |
| REQ-DEPLOY-0155 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2155–2168 | NO |
| REQ-DEPLOY-0156 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2169–2180 | NO |
| REQ-DEPLOY-0157 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2181–2188 | NO |
| REQ-CLIENT-0012 | LOCKED | Product and Deployment | Client distribution model | SRC-006 lines 2189–2206 | NO |
| REQ-DEPLOY-0158 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2207–2216 | NO |
| REQ-CLIENT-0013 | LOCKED | Product and Deployment | Client distribution model | SRC-006 lines 2217–2230 | NO |
| REQ-CLIENT-0014 | LOCKED | Product and Deployment | Client distribution model | SRC-006 lines 2231–2233 | NO |
| REQ-CLIENT-0015 | LOCKED | Product and Deployment | Client distribution model | SRC-006 lines 2234–2242 | NO |
| REQ-CLIENT-0016 | LOCKED | Product and Deployment | Client distribution model | SRC-006 lines 2243–2250 | NO |
| REQ-CLIENT-0017 | LOCKED | Product and Deployment | Client distribution model | SRC-006 lines 2251–2253 | NO |
| REQ-CLIENT-0018 | LOCKED | Product and Deployment | Client distribution model | SRC-006 lines 2254–2261 | NO |
| REQ-CLIENT-0019 | LOCKED | Product and Deployment | Client distribution model | SRC-006 lines 2262–2271 | NO |
| REQ-DEPLOY-0159 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2272–2279 | NO |
| REQ-DEPLOY-0160 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2280–2295 | NO |
| REQ-DEPLOY-0161 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2296–2304 | NO |
| REQ-DEPLOY-0162 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2305–2307 | NO |
| REQ-CLIENT-0020 | LOCKED | Product and Deployment | Client distribution model | SRC-006 lines 2308–2315 | NO |
| REQ-DEPLOY-0163 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2316–2318 | NO |
| REQ-DEPLOY-0164 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2319–2328 | NO |
| REQ-DEPLOY-0165 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2329–2337 | NO |
| REQ-DEPLOY-0166 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2338–2345 | NO |
| REQ-SEC-0014 | LOCKED | Deployment and Security | Security baseline | SRC-006 lines 2346–2354 | NO |
| REQ-DEPLOY-0167 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2355–2369 | NO |
| REQ-DEPLOY-0168 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2370–2381 | NO |
| REQ-DEPLOY-0169 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2382–2390 | NO |
| REQ-CLIENT-0021 | LOCKED | Product and Deployment | Client distribution model | SRC-006 lines 2391–2398 | NO |
| REQ-DEPLOY-0170 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2399–2406 | NO |
| REQ-DEPLOY-0171 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2407–2414 | NO |
| REQ-DEPLOY-0172 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2415–2421 | NO |
| REQ-DEPLOY-0173 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2422–2428 | NO |
| REQ-SEC-0015 | LOCKED | Deployment and Security | Security baseline | SRC-006 lines 2429–2446 | NO |
| REQ-SEC-0016 | LOCKED | Deployment and Security | Security baseline | SRC-006 lines 2447–2449 | NO |
| REQ-DEPLOY-0174 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2450–2452 | NO |
| REQ-SEC-0017 | LOCKED | Deployment and Security | Security baseline | SRC-006 lines 2453–2463 | NO |
| REQ-DEPLOY-0175 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2464–2472 | NO |
| REQ-DEPLOY-0176 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2473–2480 | NO |
| REQ-DEPLOY-0177 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2481–2490 | NO |
| REQ-OPS-0015 | LOCKED | Operations and Monitoring | Failure/recovery runbooks | SRC-006 lines 2491–2526 | NO |
| REQ-DEPLOY-0178 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2527–2538 | NO |
| REQ-DEPLOY-0179 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2539–2551 | NO |
| REQ-DEPLOY-0180 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2552–2559 | NO |
| REQ-OPS-0016 | LOCKED | Operations and Monitoring | Failure/recovery runbooks | SRC-006 lines 2560–2567 | NO |
| REQ-CLIENT-0022 | LOCKED | Product and Deployment | Client distribution model | SRC-006 lines 2568–2581 | NO |
| REQ-DEPLOY-0181 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2582–2589 | NO |
| REQ-DEPLOY-0182 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2590–2605 | NO |
| REQ-DEPLOY-0183 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2606–2615 | NO |
| REQ-DEPLOY-0184 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2616–2623 | NO |
| REQ-DEPLOY-0185 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2624–2632 | NO |
| REQ-LIC-0005 | LOCKED | Deployment and Security | License contract | SRC-006 lines 2633–2647 | NO |
| REQ-CLIENT-0023 | LOCKED | Product and Deployment | Client distribution model | SRC-006 lines 2648–2659 | NO |
| REQ-SEC-0018 | LOCKED | Deployment and Security | Security baseline | SRC-006 lines 2660–2666 | NO |
| REQ-DEPLOY-0186 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2667–2680 | NO |
| REQ-DEPLOY-0187 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2681–2692 | NO |
| REQ-DEPLOY-0188 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2693–2700 | NO |
| REQ-DEPLOY-0189 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2701–2709 | NO |
| REQ-DEPLOY-0190 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2710–2722 | NO |
| REQ-DEPLOY-0191 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2723–2733 | NO |
| REQ-DEPLOY-0192 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2734–2747 | NO |
| REQ-OPS-0017 | LOCKED | Operations and Monitoring | Failure/recovery runbooks | SRC-006 lines 2748–2754 | NO |
| REQ-DEPLOY-0193 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2755–2764 | NO |
| REQ-DEPLOY-0194 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2765–2814 | NO |
| REQ-DEPLOY-0195 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2815–2842 | NO |
| REQ-SEC-0019 | LOCKED | Deployment and Security | Security baseline | SRC-006 lines 2843–2859 | NO |
| REQ-DEPLOY-0196 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2860–2868 | NO |
| REQ-DEPLOY-0197 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2869–2887 | NO |
| REQ-DEPLOY-0198 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2888–2900 | NO |
| REQ-DEPLOY-0199 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2901–2912 | NO |
| REQ-DEPLOY-0200 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2913–2924 | NO |
| REQ-DEPLOY-0201 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2925–2933 | NO |
| REQ-SEC-0020 | LOCKED | Deployment and Security | Security baseline | SRC-006 lines 2934–2948 | NO |
| REQ-DEPLOY-0202 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2949–2962 | NO |
| REQ-DEPLOY-0203 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2963–2972 | NO |
| REQ-DEPLOY-0204 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2973–2980 | NO |
| REQ-DEPLOY-0205 | FUTURE | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2981–2988 | NO |
| REQ-DEPLOY-0206 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 2989–3003 | NO |
| REQ-CLIENT-0024 | LOCKED | Product and Deployment | Client distribution model | SRC-006 lines 3004–3036 | NO |
| REQ-DEPLOY-0207 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 3037–3069 | NO |
| REQ-LIC-0006 | LOCKED | Deployment and Security | License contract | SRC-006 lines 3070–3087 | NO |
| REQ-DEPLOY-0208 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 3088–3113 | NO |
| REQ-DEPLOY-0209 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 3114–3134 | NO |
| REQ-DEPLOY-0210 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 3135–3246 | NO |
| REQ-DEPLOY-0211 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 3247–3338 | NO |
| REQ-LIC-0007 | LOCKED | Deployment and Security | License contract | SRC-006 lines 3339–3392 | NO |
| REQ-DEPLOY-0212 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 3393–3427 | NO |
| REQ-DEPLOY-0213 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 3428–3501 | NO |
| REQ-DEPLOY-0214 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 3502–3544 | NO |
| REQ-DEPLOY-0215 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-006 lines 3545–3594 | NO |
| REQ-VALID-0015 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3595–3596 | NO |
| REQ-VALID-0016 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3597–3638 | NO |
| REQ-VALID-0017 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3639–3647 | NO |
| REQ-VALID-0018 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3648–3660 | NO |
| REQ-VALID-0019 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3661–3668 | NO |
| REQ-VALID-0020 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3669–3675 | NO |
| REQ-VALID-0021 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3676–3687 | NO |
| REQ-VALID-0022 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3688–3702 | NO |
| REQ-VALID-0023 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3703–3711 | NO |
| REQ-VALID-0024 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3712–3728 | NO |
| REQ-VALID-0025 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3729–3741 | NO |
| REQ-VALID-0026 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3742–3748 | NO |
| REQ-VALID-0027 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3749–3800 | NO |
| REQ-VALID-0028 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3801–3828 | NO |
| REQ-VALID-0029 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3829–3838 | NO |
| REQ-VALID-0030 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3839–3847 | NO |
| REQ-VALID-0031 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3848–3851 | NO |
| REQ-VALID-0032 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3852–3861 | NO |
| REQ-VALID-0033 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3862–3882 | NO |
| REQ-VALID-0034 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3883–3887 | NO |
| REQ-VALID-0035 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3888–3893 | NO |
| REQ-VALID-0036 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3894–3901 | NO |
| REQ-VALID-0037 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3902–3935 | NO |
| REQ-VALID-0038 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3936–3938 | NO |
| REQ-VALID-0039 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3939–3946 | NO |
| REQ-VALID-0040 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3947–3951 | NO |
| REQ-VALID-0041 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3952–3956 | NO |
| REQ-VALID-0042 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3957–3961 | NO |
| REQ-VALID-0043 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3962–3972 | NO |
| REQ-VALID-0044 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3973–3977 | NO |
| REQ-VALID-0045 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3978–3986 | NO |
| REQ-VALID-0046 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3987–3991 | NO |
| REQ-VALID-0047 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3992–3998 | NO |
| REQ-VALID-0048 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 3999–4003 | NO |
| REQ-VALID-0049 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4004–4007 | NO |
| REQ-VALID-0050 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4008–4016 | NO |
| REQ-VALID-0051 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4017–4019 | NO |
| REQ-VALID-0052 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4020–4029 | NO |
| REQ-VALID-0053 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4030–4032 | NO |
| REQ-VALID-0054 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4033–4058 | NO |
| REQ-VALID-0055 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4059–4066 | NO |
| REQ-VALID-0056 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4067–4072 | NO |
| REQ-VALID-0057 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4073–4096 | NO |
| REQ-VALID-0058 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4097–4103 | NO |
| REQ-VALID-0059 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4104–4107 | NO |
| REQ-VALID-0060 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4108–4114 | NO |
| REQ-VALID-0061 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4115–4125 | NO |
| REQ-VALID-0062 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4126–4132 | NO |
| REQ-VALID-0063 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4133–4137 | NO |
| REQ-VALID-0064 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4138–4175 | NO |
| REQ-VALID-0065 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4176–4186 | NO |
| REQ-VALID-0066 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4187–4191 | NO |
| REQ-VALID-0067 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4192–4197 | NO |
| REQ-VALID-0068 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4198–4204 | NO |
| REQ-VALID-0069 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4205–4209 | NO |
| REQ-VALID-0070 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4210–4216 | NO |
| REQ-VALID-0071 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4217–4223 | NO |
| REQ-VALID-0072 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4224–4242 | NO |
| REQ-VALID-0073 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4243–4248 | NO |
| REQ-VALID-0074 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4249–4253 | NO |
| REQ-VALID-0075 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4254–4257 | NO |
| REQ-VALID-0076 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4258–4268 | NO |
| REQ-VALID-0077 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4269–4274 | NO |
| REQ-VALID-0078 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4275–4277 | NO |
| REQ-VALID-0079 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4278–4283 | NO |
| REQ-VALID-0080 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4284–4288 | NO |
| REQ-VALID-0081 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4289–4306 | NO |
| REQ-VALID-0082 | CALIBRATED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4307–4312 | NO |
| REQ-VALID-0083 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4313–4319 | NO |
| REQ-VALID-0084 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4320–4326 | NO |
| REQ-VALID-0085 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4327–4332 | NO |
| REQ-VALID-0086 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4333–4338 | NO |
| REQ-VALID-0087 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4339–4342 | NO |
| REQ-VALID-0088 | RESEARCH | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4343–4345 | NO |
| REQ-VALID-0089 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4346–4352 | NO |
| REQ-VALID-0090 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4353–4362 | NO |
| REQ-VALID-0091 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4363–4368 | NO |
| REQ-VALID-0092 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4369–4373 | NO |
| REQ-VALID-0093 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4374–4383 | NO |
| REQ-VALID-0094 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4384–4387 | NO |
| REQ-VALID-0095 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4388–4392 | NO |
| REQ-VALID-0096 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4393–4396 | NO |
| REQ-VALID-0097 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4397–4404 | NO |
| REQ-VALID-0098 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4405–4411 | NO |
| REQ-VALID-0099 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4412–4416 | NO |
| REQ-VALID-0100 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4417–4422 | NO |
| REQ-VALID-0101 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4423–4425 | NO |
| REQ-VALID-0102 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4426–4466 | NO |
| REQ-VALID-0103 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4467–4471 | NO |
| REQ-VALID-0104 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4472–4479 | NO |
| REQ-VALID-0105 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4480–4482 | NO |
| REQ-VALID-0106 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4483–4485 | NO |
| REQ-VALID-0107 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4486–4491 | NO |
| REQ-VALID-0108 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4492–4494 | NO |
| REQ-VALID-0109 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4495–4514 | NO |
| REQ-VALID-0110 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4515–4520 | NO |
| REQ-VALID-0111 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4521–4527 | NO |
| REQ-VALID-0112 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4528–4532 | NO |
| REQ-VALID-0113 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4533–4536 | NO |
| REQ-VALID-0114 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4537–4539 | NO |
| REQ-VALID-0115 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4540–4543 | NO |
| REQ-VALID-0116 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4544–4549 | NO |
| REQ-VALID-0117 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4550–4556 | NO |
| REQ-VALID-0118 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4557–4559 | NO |
| REQ-VALID-0119 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4560–4562 | NO |
| REQ-VALID-0120 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4563–4565 | NO |
| REQ-VALID-0121 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4566–4568 | NO |
| REQ-VALID-0122 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4569–4571 | NO |
| REQ-VALID-0123 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4572–4574 | NO |
| REQ-VALID-0124 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4575–4582 | NO |
| REQ-VALID-0125 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4583–4589 | NO |
| REQ-VALID-0126 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4590–4603 | NO |
| REQ-VALID-0127 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4604–4606 | NO |
| REQ-VALID-0128 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4607–4610 | NO |
| REQ-VALID-0129 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4611–4613 | NO |
| REQ-VALID-0130 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4614–4617 | NO |
| REQ-VALID-0131 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4618–4623 | NO |
| REQ-VALID-0132 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4624–4630 | NO |
| REQ-VALID-0133 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4631–4635 | NO |
| REQ-VALID-0134 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4636–4638 | NO |
| REQ-VALID-0135 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4639–4641 | NO |
| REQ-VALID-0136 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4642–4650 | NO |
| REQ-VALID-0137 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4651–4655 | NO |
| REQ-VALID-0138 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4656–4659 | NO |
| REQ-VALID-0139 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4660–4667 | NO |
| REQ-VALID-0140 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4668–4672 | NO |
| REQ-VALID-0141 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4673–4677 | NO |
| REQ-VALID-0142 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4678–4680 | NO |
| REQ-VALID-0143 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4681–4687 | NO |
| REQ-VALID-0144 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4688–4720 | NO |
| REQ-VALID-0145 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4721–4723 | NO |
| REQ-VALID-0146 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4724–4727 | NO |
| REQ-VALID-0147 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4728–4731 | NO |
| REQ-VALID-0148 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4732–4734 | NO |
| REQ-VALID-0149 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4735–4740 | NO |
| REQ-VALID-0150 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4741–4746 | NO |
| REQ-VALID-0151 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4747–4752 | NO |
| REQ-VALID-0152 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4753–4755 | NO |
| REQ-VALID-0153 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4756–4758 | NO |
| REQ-VALID-0154 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4759–4763 | NO |
| REQ-VALID-0155 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4764–4767 | NO |
| REQ-VALID-0156 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4768–4784 | NO |
| REQ-VALID-0157 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4785–4791 | NO |
| REQ-VALID-0158 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4792–4794 | NO |
| REQ-VALID-0159 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4795–4801 | NO |
| REQ-VALID-0160 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4802–4806 | NO |
| REQ-VALID-0161 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4807–4813 | NO |
| REQ-VALID-0162 | CALIBRATED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4814–4821 | NO |
| REQ-VALID-0163 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4822–4835 | NO |
| REQ-VALID-0164 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4836–4839 | NO |
| REQ-VALID-0165 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4840–4845 | NO |
| REQ-VALID-0166 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4846–4859 | NO |
| REQ-VALID-0167 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4860–4864 | NO |
| REQ-VALID-0168 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4865–4867 | NO |
| REQ-VALID-0169 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4868–4882 | NO |
| REQ-VALID-0170 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4883–4914 | NO |
| REQ-VALID-0171 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4915–4917 | NO |
| REQ-VALID-0172 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4918–4925 | NO |
| REQ-VALID-0173 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4926–4935 | NO |
| REQ-VALID-0174 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4936–4942 | NO |
| REQ-VALID-0175 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4943–4947 | NO |
| REQ-VALID-0176 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4948–4952 | NO |
| REQ-VALID-0177 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4953–4957 | NO |
| REQ-VALID-0178 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4958–4961 | NO |
| REQ-VALID-0179 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4962–4985 | NO |
| REQ-VALID-0180 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4986–4989 | NO |
| REQ-VALID-0181 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4990–4996 | NO |
| REQ-VALID-0182 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 4997–5000 | NO |
| REQ-VALID-0183 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5001–5006 | NO |
| REQ-VALID-0184 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5007–5012 | NO |
| REQ-VALID-0185 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5013–5015 | NO |
| REQ-VALID-0186 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5016–5031 | NO |
| REQ-VALID-0187 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5032–5042 | NO |
| REQ-VALID-0188 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5043–5047 | NO |
| REQ-VALID-0189 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5048–5052 | NO |
| REQ-VALID-0190 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5053–5064 | NO |
| REQ-VALID-0191 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5065–5070 | NO |
| REQ-VALID-0192 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5071–5076 | NO |
| REQ-VALID-0193 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5077–5082 | NO |
| REQ-VALID-0194 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5083–5087 | NO |
| REQ-VALID-0195 | RESEARCH | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5088–5117 | NO |
| REQ-VALID-0196 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5118–5123 | NO |
| REQ-VALID-0197 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5124–5128 | NO |
| REQ-VALID-0198 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5129–5131 | NO |
| REQ-VALID-0199 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5132–5183 | NO |
| REQ-VALID-0200 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5184–5204 | NO |
| REQ-VALID-0201 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5205–5217 | NO |
| REQ-VALID-0202 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5218–5220 | NO |
| REQ-VALID-0203 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5221–5225 | NO |
| REQ-VALID-0204 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5226–5228 | NO |
| REQ-VALID-0205 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5229–5231 | NO |
| REQ-VALID-0206 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5232–5234 | NO |
| REQ-VALID-0207 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5235–5242 | NO |
| REQ-VALID-0208 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5243–5248 | NO |
| REQ-VALID-0209 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5249–5251 | NO |
| REQ-VALID-0210 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5252–5254 | NO |
| REQ-VALID-0211 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5255–5257 | NO |
| REQ-VALID-0212 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5258–5263 | NO |
| REQ-VALID-0213 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5264–5272 | NO |
| REQ-VALID-0214 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5273–5279 | NO |
| REQ-VALID-0215 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5280–5284 | NO |
| REQ-VALID-0216 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5285–5287 | NO |
| REQ-VALID-0217 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5288–5290 | NO |
| REQ-VALID-0218 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5291–5293 | NO |
| REQ-VALID-0219 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5294–5301 | NO |
| REQ-VALID-0220 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5302–5305 | NO |
| REQ-VALID-0221 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5306–5316 | NO |
| REQ-VALID-0222 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5317–5329 | NO |
| REQ-VALID-0223 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5330–5337 | NO |
| REQ-VALID-0224 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5338–5340 | NO |
| REQ-VALID-0225 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5341–5345 | NO |
| REQ-VALID-0226 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5346–5348 | NO |
| REQ-VALID-0227 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5349–5356 | NO |
| REQ-VALID-0228 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5357–5364 | NO |
| REQ-VALID-0229 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5365–5374 | NO |
| REQ-VALID-0230 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5375–5377 | NO |
| REQ-VALID-0231 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5378–5381 | NO |
| REQ-VALID-0232 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5382–5388 | NO |
| REQ-VALID-0233 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5389–5395 | NO |
| REQ-VALID-0234 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5396–5406 | NO |
| REQ-VALID-0235 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5407–5417 | NO |
| REQ-VALID-0236 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5418–5426 | NO |
| REQ-VALID-0237 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5427–5432 | NO |
| REQ-VALID-0238 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5433–5435 | NO |
| REQ-VALID-0239 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5436–5442 | NO |
| REQ-VALID-0240 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5443–5449 | NO |
| REQ-VALID-0241 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5450–5455 | NO |
| REQ-VALID-0242 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5456–5464 | NO |
| REQ-VALID-0243 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5465–5467 | NO |
| REQ-VALID-0244 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5468–5471 | NO |
| REQ-VALID-0245 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5472–5474 | NO |
| REQ-VALID-0246 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5475–5480 | NO |
| REQ-VALID-0247 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5481–5485 | NO |
| REQ-VALID-0248 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5486–5489 | NO |
| REQ-VALID-0249 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5490–5527 | NO |
| REQ-VALID-0250 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5528–5531 | NO |
| REQ-VALID-0251 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5532–5538 | NO |
| REQ-VALID-0252 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5539–5544 | NO |
| REQ-VALID-0253 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5545–5547 | NO |
| REQ-VALID-0254 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5548–5553 | NO |
| REQ-VALID-0255 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5554–5559 | NO |
| REQ-VALID-0256 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5560–5564 | NO |
| REQ-VALID-0257 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5565–5569 | NO |
| REQ-VALID-0258 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5570–5574 | NO |
| REQ-VALID-0259 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5575–5579 | NO |
| REQ-VALID-0260 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5580–5587 | NO |
| REQ-VALID-0261 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5588–5590 | NO |
| REQ-VALID-0262 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5591–5593 | NO |
| REQ-VALID-0263 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5594–5596 | NO |
| REQ-VALID-0264 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5597–5599 | NO |
| REQ-VALID-0265 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5600–5610 | NO |
| REQ-VALID-0266 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5611–5616 | NO |
| REQ-VALID-0267 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5617–5624 | NO |
| REQ-VALID-0268 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5625–5632 | NO |
| REQ-VALID-0269 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5633–5637 | NO |
| REQ-VALID-0270 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5638–5642 | NO |
| REQ-VALID-0271 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5643–5653 | NO |
| REQ-VALID-0272 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5654–5656 | NO |
| REQ-VALID-0273 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5657–5710 | NO |
| REQ-VALID-0274 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5711–5714 | NO |
| REQ-VALID-0275 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5715–5717 | NO |
| REQ-VALID-0276 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5718–5723 | NO |
| REQ-VALID-0277 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5724–5726 | NO |
| REQ-VALID-0278 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5727–5731 | NO |
| REQ-VALID-0279 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5732–5740 | NO |
| REQ-VALID-0280 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5741–5743 | NO |
| REQ-VALID-0281 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5744–5746 | NO |
| REQ-VALID-0282 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5747–5749 | NO |
| REQ-VALID-0283 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5750–5752 | NO |
| REQ-VALID-0284 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5753–5755 | NO |
| REQ-VALID-0285 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5756–5758 | NO |
| REQ-VALID-0286 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5759–5764 | NO |
| REQ-VALID-0287 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5765–5775 | NO |
| REQ-VALID-0288 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5776–5782 | NO |
| REQ-VALID-0289 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5783–5787 | NO |
| REQ-VALID-0290 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5788–5805 | NO |
| REQ-VALID-0291 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5806–5809 | NO |
| REQ-VALID-0292 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5810–5812 | NO |
| REQ-VALID-0293 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5813–5817 | NO |
| REQ-VALID-0294 | RESEARCH | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5818–5824 | NO |
| REQ-VALID-0295 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5825–5830 | NO |
| REQ-VALID-0296 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5831–5836 | NO |
| REQ-VALID-0297 | REJECTED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5837–5841 | NO |
| REQ-VALID-0298 | RESEARCH | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5842–5846 | NO |
| REQ-VALID-0299 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5847–5850 | NO |
| REQ-VALID-0300 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5851–5854 | NO |
| REQ-VALID-0301 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5855–5858 | NO |
| REQ-VALID-0302 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5859–5868 | NO |
| REQ-VALID-0303 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5869–5871 | NO |
| REQ-VALID-0304 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5872–5876 | NO |
| REQ-VALID-0305 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5877–5880 | NO |
| REQ-VALID-0306 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5881–5883 | NO |
| REQ-VALID-0307 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5884–5890 | NO |
| REQ-VALID-0308 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5891–5914 | NO |
| REQ-VALID-0309 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5915–5935 | NO |
| REQ-VALID-0310 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5936–5938 | NO |
| REQ-VALID-0311 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5939–5942 | NO |
| REQ-VALID-0312 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5943–5948 | NO |
| REQ-VALID-0313 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5949–5951 | NO |
| REQ-VALID-0314 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5952–5954 | NO |
| REQ-VALID-0315 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5955–5957 | NO |
| REQ-VALID-0316 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5958–5975 | NO |
| REQ-VALID-0317 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5976–5985 | NO |
| REQ-VALID-0318 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5986–5993 | NO |
| REQ-VALID-0319 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 5994–6002 | NO |
| REQ-VALID-0320 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6003–6010 | NO |
| REQ-VALID-0321 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6011–6016 | NO |
| REQ-VALID-0322 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6017–6031 | NO |
| REQ-VALID-0323 | RESEARCH | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6032–6036 | NO |
| REQ-VALID-0324 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6037–6045 | NO |
| REQ-VALID-0325 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6046–6050 | NO |
| REQ-VALID-0326 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6051–6058 | NO |
| REQ-VALID-0327 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6059–6076 | NO |
| REQ-VALID-0328 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6077–6082 | NO |
| REQ-VALID-0329 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6083–6086 | NO |
| REQ-VALID-0330 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6087–6099 | NO |
| REQ-VALID-0331 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6100–6102 | NO |
| REQ-VALID-0332 | RESEARCH | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6103–6109 | NO |
| REQ-VALID-0333 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6110–6114 | NO |
| REQ-VALID-0334 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6115–6118 | NO |
| REQ-VALID-0335 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6119–6125 | NO |
| REQ-VALID-0336 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6126–6130 | NO |
| REQ-VALID-0337 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6131–6143 | NO |
| REQ-VALID-0338 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6144–6155 | NO |
| REQ-VALID-0339 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6156–6158 | NO |
| REQ-VALID-0340 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6159–6162 | NO |
| REQ-VALID-0341 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6163–6169 | NO |
| REQ-VALID-0342 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6170–6174 | NO |
| REQ-VALID-0343 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6175–6181 | NO |
| REQ-VALID-0344 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6182–6192 | NO |
| REQ-VALID-0345 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6193–6201 | NO |
| REQ-VALID-0346 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6202–6211 | NO |
| REQ-VALID-0347 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6212–6219 | NO |
| REQ-VALID-0348 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6220–6222 | NO |
| REQ-VALID-0349 | CALIBRATED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6223–6248 | NO |
| REQ-VALID-0350 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6249–6262 | NO |
| REQ-VALID-0351 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6263–6269 | NO |
| REQ-VALID-0352 | RESEARCH | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6270–6278 | NO |
| REQ-VALID-0353 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6279–6284 | NO |
| REQ-VALID-0354 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6285–6303 | NO |
| REQ-VALID-0355 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6304–6330 | NO |
| REQ-VALID-0356 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6331–6334 | NO |
| REQ-VALID-0357 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6335–6338 | NO |
| REQ-VALID-0358 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6339–6430 | NO |
| REQ-VALID-0359 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6431–6457 | NO |
| REQ-VALID-0360 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6458–6464 | NO |
| REQ-VALID-0361 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6465–6474 | NO |
| REQ-VALID-0362 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6475–6562 | NO |
| REQ-VALID-0363 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6563–6580 | NO |
| REQ-VALID-0364 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6581–6595 | NO |
| REQ-VALID-0365 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6596–6672 | NO |
| REQ-VALID-0366 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6673–6743 | NO |
| REQ-VALID-0367 | LOCKED | Validation Matrix | M0–M5 evidence gates | SRC-006 lines 6744–6903 | NO |
| REQ-INFRA-0035 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-007 lines 1–16 | NO |
| REQ-QUANT-0006 | RESEARCH | Formula Book | Quant models | SRC-007 lines 17–28 | NO |
| REQ-INFRA-0036 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-007 lines 29–57 | NO |
| REQ-INFRA-0037 | EXTERNAL_REVALIDATION | Infrastructure Master | Infrastructure deep specs | SRC-007 lines 58–103 | NO |
| REQ-DEPLOY-0216 | EXTERNAL_REVALIDATION | Deployment and Docker | Client deployment lifecycle | SRC-007 lines 104–150 | NO |
| REQ-PRODUCT-0015 | EXTERNAL_REVALIDATION | Product and Scope | Product model | SRC-007 lines 151–325 | NO |
| REQ-EXEC-0240 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 328–390 | NO |
| REQ-EXEC-0241 | FUTURE | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 391–420 | NO |
| REQ-EXEC-0242 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 421–470 | NO |
| REQ-SURV-0001 | RESEARCH | Market Participants | Edge Survival | SRC-007 lines 471–508 | NO |
| REQ-EXEC-0243 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 509–582 | NO |
| REQ-ACCT-0049 | RESEARCH | Accounting | PnL attribution | SRC-007 lines 583–629 | NO |
| REQ-RISK-0299 | EXTERNAL_REVALIDATION | Risk Constitution | Risk gates and budgets | SRC-007 lines 630–659 | NO |
| REQ-FUTURE-0005 | EXTERNAL_REVALIDATION | Future Architecture | Future capability register | SRC-007 lines 660–688 | NO |
| REQ-SURV-0002 | RESEARCH | Market Participants | Edge Survival | SRC-007 lines 689–739 | NO |
| REQ-SURV-0003 | RESEARCH | Market Participants | Edge Survival | SRC-007 lines 740–792 | NO |
| REQ-INFRA-0038 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-007 lines 793–914 | NO |
| REQ-EXEC-0244 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 915–935 | NO |
| REQ-SURV-0004 | FUTURE | Market Participants | Edge Survival | SRC-007 lines 936–969 | NO |
| REQ-SURV-0005 | RESEARCH | Market Participants | Edge Survival | SRC-007 lines 970–1013 | NO |
| REQ-EXEC-0245 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 1014–1056 | NO |
| REQ-EXEC-0246 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 1057–1083 | NO |
| REQ-MICRO-0006 | CALIBRATED | Market Microstructure | OFI/MLOFI/queue | SRC-007 lines 1084–1157 | NO |
| REQ-MICRO-0007 | EXTERNAL_REVALIDATION | Market Microstructure | OFI/MLOFI/queue | SRC-007 lines 1158–1199 | NO |
| REQ-MICRO-0008 | RESEARCH | Market Microstructure | OFI/MLOFI/queue | SRC-007 lines 1200–1225 | NO |
| REQ-PART-0001 | EXTERNAL_REVALIDATION | Market Participants | Participant response model | SRC-007 lines 1226–1247 | NO |
| REQ-PART-0002 | EXTERNAL_REVALIDATION | Market Participants | Participant response model | SRC-007 lines 1248–1262 | NO |
| REQ-EXEC-0247 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 1263–1292 | NO |
| REQ-XMARKET-0001 | RESEARCH | Market Participants | Cross-Market Response | SRC-007 lines 1293–1340 | NO |
| REQ-PRODUCT-0016 | CALIBRATED | Product and Scope | Product model | SRC-007 lines 1341–1386 | NO |
| REQ-ACCT-0050 | RESEARCH | Accounting | PnL attribution | SRC-007 lines 1387–1407 | NO |
| REQ-XMARKET-0002 | RESEARCH | Market Participants | Cross-Market Response | SRC-007 lines 1408–1494 | NO |
| REQ-LIQ-0001 | EXTERNAL_REVALIDATION | Market Participants | Liquidity Response | SRC-007 lines 1495–1527 | NO |
| REQ-EXEC-0248 | FUTURE | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 1528–1550 | NO |
| REQ-MICRO-0009 | RESEARCH | Market Microstructure | OFI/MLOFI/queue | SRC-007 lines 1551–1676 | NO |
| REQ-LIQ-0002 | RESEARCH | Market Participants | Liquidity Response | SRC-007 lines 1677–1762 | NO |
| REQ-SLICE-0003 | LOCKED | Execution State Machine | Order Slicing | SRC-007 lines 1763–1877 | NO |
| REQ-EXEC-0249 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 1878–1907 | NO |
| REQ-LIQ-0003 | FUTURE | Market Participants | Liquidity Response | SRC-007 lines 1908–1980 | NO |
| REQ-EXEC-0250 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 1981–2004 | NO |
| REQ-EXEC-0251 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 2005–2111 | NO |
| REQ-EXEC-0252 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 2112–2205 | NO |
| REQ-QUANT-0007 | FUTURE | Formula Book | Quant models | SRC-007 lines 2206–2246 | NO |
| REQ-FUTURE-0006 | FUTURE | Future Architecture | Future capability register | SRC-007 lines 2247–2248 | NO |
| REQ-SURV-0006 | RESEARCH | Market Participants | Edge Survival | SRC-007 lines 2249–2256 | NO |
| REQ-FUTURE-0007 | FUTURE | Future Architecture | Future capability register | SRC-007 lines 2257–2261 | NO |
| REQ-FUTURE-0008 | FUTURE | Future Architecture | Future capability register | SRC-007 lines 2262–2266 | NO |
| REQ-FUTURE-0009 | FUTURE | Future Architecture | Future capability register | SRC-007 lines 2267–2271 | NO |
| REQ-RESEARCH-0016 | RESEARCH | Research Appendix | Research candidates | SRC-007 lines 2272–2285 | NO |
| REQ-XMARKET-0003 | RESEARCH | Market Participants | Cross-Market Response | SRC-007 lines 2286–2306 | NO |
| REQ-XMARKET-0004 | RESEARCH | Market Participants | Cross-Market Response | SRC-007 lines 2307–2370 | NO |
| REQ-XMARKET-0005 | REJECTED | Market Participants | Cross-Market Response | SRC-007 lines 2371–2409 | NO |
| REQ-XMARKET-0006 | RESEARCH | Market Participants | Cross-Market Response | SRC-007 lines 2410–2469 | NO |
| REQ-EXEC-0253 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 2470–2488 | NO |
| REQ-XMARKET-0007 | RESEARCH | Market Participants | Cross-Market Response | SRC-007 lines 2489–2547 | NO |
| REQ-XMARKET-0008 | RESEARCH | Market Participants | Cross-Market Response | SRC-007 lines 2548–2560 | NO |
| REQ-XMARKET-0009 | RESEARCH | Market Participants | Cross-Market Response | SRC-007 lines 2561–2587 | NO |
| REQ-PART-0003 | RESEARCH | Market Participants | Participant response model | SRC-007 lines 2588–2624 | NO |
| REQ-EXEC-0254 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 2625–2649 | NO |
| REQ-PART-0004 | LOCKED | Market Participants | Participant response model | SRC-007 lines 2650–2693 | NO |
| REQ-INFRA-0039 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-007 lines 2694–2746 | NO |
| REQ-PRODUCT-0017 | CALIBRATED | Product and Scope | Product model | SRC-007 lines 2747–2810 | NO |
| REQ-PART-0005 | RESEARCH | Market Participants | Participant response model | SRC-007 lines 2811–2963 | NO |
| REQ-SURV-0007 | LOCKED | Market Participants | Edge Survival | SRC-007 lines 2964–2999 | NO |
| REQ-SIM-0001 | RESEARCH | Counterfactual Simulator | Simulator fidelities and models | SRC-007 lines 3000–3072 | NO |
| REQ-EXEC-0255 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 3073–3104 | NO |
| REQ-PART-0006 | RESEARCH | Market Participants | Participant response model | SRC-007 lines 3105–3106 | NO |
| REQ-ARCH-0073 | RESEARCH | Master Architecture | Architecture modules | SRC-007 lines 3107–3116 | NO |
| REQ-PART-0007 | RESEARCH | Market Participants | Participant response model | SRC-007 lines 3117–3126 | NO |
| REQ-MICRO-0010 | RESEARCH | Market Microstructure | OFI/MLOFI/queue | SRC-007 lines 3127–3194 | NO |
| REQ-QUANT-0008 | RESEARCH | Formula Book | Quant models | SRC-007 lines 3195–3299 | NO |
| REQ-RISK-0300 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-007 lines 3300–3324 | NO |
| REQ-PART-0008 | RESEARCH | Market Participants | Participant response model | SRC-007 lines 3325–3358 | NO |
| REQ-FUTURE-0010 | FUTURE | Future Architecture | Future capability register | SRC-007 lines 3359–3396 | NO |
| REQ-EXEC-0256 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 3397–3445 | NO |
| REQ-PART-0009 | FUTURE | Market Participants | Participant response model | SRC-007 lines 3446–3485 | NO |
| REQ-DATA-0316 | RESEARCH | Data Contracts | Schemas and event contracts | SRC-007 lines 3486–3495 | NO |
| REQ-RISK-0301 | OPEN | Risk Constitution | Risk gates and budgets | SRC-007 lines 3496–3514 | NO |
| REQ-EXEC-0257 | FUTURE | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 3515–3539 | NO |
| REQ-DATA-0317 | LOCKED | Data Contracts | Schemas and event contracts | SRC-007 lines 3540–3573 | NO |
| REQ-ARCH-0074 | REJECTED | Master Architecture | Architecture modules | SRC-007 lines 3574–3591 | NO |
| REQ-CLOCK-0014 | CALIBRATED | Data Contracts | Clock and RNG contract | SRC-007 lines 3592–3619 | NO |
| REQ-ACCT-0051 | RESEARCH | Accounting | PnL attribution | SRC-007 lines 3620–3641 | NO |
| REQ-SURV-0008 | RESEARCH | Market Participants | Edge Survival | SRC-007 lines 3642–3666 | NO |
| REQ-SURV-0009 | RESEARCH | Market Participants | Edge Survival | SRC-007 lines 3667–3723 | NO |
| REQ-SURV-0010 | FUTURE | Market Participants | Edge Survival | SRC-007 lines 3724–3740 | NO |
| REQ-SURV-0011 | RESEARCH | Market Participants | Edge Survival | SRC-007 lines 3741–3756 | NO |
| REQ-VALID-0368 | RESEARCH | Validation Matrix | M0–M5 evidence gates | SRC-007 lines 3757–3784 | NO |
| REQ-VALID-0369 | RESEARCH | Validation Matrix | M0–M5 evidence gates | SRC-007 lines 3785–3811 | NO |
| REQ-QUANT-0009 | RESEARCH | Formula Book | Quant models | SRC-007 lines 3812–3835 | NO |
| REQ-ACCT-0052 | RESEARCH | Accounting | PnL attribution | SRC-007 lines 3836–3852 | NO |
| REQ-ACCT-0053 | RESEARCH | Accounting | PnL attribution | SRC-007 lines 3853–3854 | NO |
| REQ-ARCH-0075 | CALIBRATED | Master Architecture | Architecture modules | SRC-007 lines 3855–3859 | NO |
| REQ-EXEC-0258 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 3860–3917 | NO |
| REQ-VALID-0370 | RESEARCH | Validation Matrix | M0–M5 evidence gates | SRC-007 lines 3918–3941 | NO |
| REQ-INFRA-0040 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-007 lines 3942–3957 | NO |
| REQ-SURV-0012 | CALIBRATED | Market Participants | Edge Survival | SRC-007 lines 3958–4001 | NO |
| REQ-PART-0010 | LOCKED | Market Participants | Participant response model | SRC-007 lines 4002–4026 | NO |
| REQ-OPS-0018 | RESEARCH | Operations and Monitoring | Failure/recovery runbooks | SRC-007 lines 4027–4045 | NO |
| REQ-PRODUCT-0018 | RESEARCH | Product and Scope | Product model | SRC-007 lines 4046–4067 | NO |
| REQ-PRODUCT-0019 | FUTURE | Product and Scope | Product model | SRC-007 lines 4068–4092 | NO |
| REQ-DATA-0318 | RESEARCH | Data Contracts | Schemas and event contracts | SRC-007 lines 4093–4114 | NO |
| REQ-ROUTE-0028 | LOCKED | Market Graph and Routes | Route/NetConvert contracts | SRC-007 lines 4115–4143 | NO |
| REQ-SIM-0002 | RESEARCH | Counterfactual Simulator | Simulator fidelities and models | SRC-007 lines 4144–4159 | NO |
| REQ-ARCH-0076 | RESEARCH | Master Architecture | Architecture modules | SRC-007 lines 4160–4181 | NO |
| REQ-SIM-0003 | FUTURE | Counterfactual Simulator | Simulator fidelities and models | SRC-007 lines 4182–4195 | NO |
| REQ-ARCH-0077 | RESEARCH | Master Architecture | Architecture modules | SRC-007 lines 4196–4216 | NO |
| REQ-BENCH-0006 | CALIBRATED | Infrastructure Master | Benchmark Protocol | SRC-007 lines 4217–4237 | NO |
| REQ-LIQ-0004 | RESEARCH | Market Participants | Liquidity Response | SRC-007 lines 4238–4255 | NO |
| REQ-EXEC-0259 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 4256–4276 | NO |
| REQ-XMARKET-0010 | RESEARCH | Market Participants | Cross-Market Response | SRC-007 lines 4277–4291 | NO |
| REQ-PART-0011 | RESEARCH | Market Participants | Participant response model | SRC-007 lines 4292–4307 | NO |
| REQ-HWC-0028 | RESEARCH | Master Architecture | Activation policy | SRC-007 lines 4308–4309 | NO |
| REQ-HWC-0029 | RESEARCH | Master Architecture | Activation policy | SRC-007 lines 4310–4318 | NO |
| REQ-HWC-0030 | RESEARCH | Master Architecture | Activation policy | SRC-007 lines 4319–4326 | NO |
| REQ-HWC-0031 | RESEARCH | Master Architecture | Activation policy | SRC-007 lines 4327–4334 | NO |
| REQ-INFRA-0041 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-007 lines 4335–4352 | NO |
| REQ-PART-0012 | FUTURE | Market Participants | Participant response model | SRC-007 lines 4353–4444 | NO |
| REQ-PART-0013 | RESEARCH | Market Participants | Participant response model | SRC-007 lines 4445–4519 | NO |
| REQ-INFRA-0042 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-007 lines 4520–4580 | NO |
| REQ-PART-0014 | RESEARCH | Market Participants | Participant response model | SRC-007 lines 4581–4614 | NO |
| REQ-PART-0015 | RESEARCH | Market Participants | Participant response model | SRC-007 lines 4615–4646 | NO |
| REQ-RECOV-0016 | RESEARCH | Execution State Machine | Recovery and Unknown State | SRC-007 lines 4647–4672 | NO |
| REQ-EXEC-0260 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 4673–4685 | NO |
| REQ-PART-0016 | RESEARCH | Market Participants | Participant response model | SRC-007 lines 4686–4715 | NO |
| REQ-SIM-0004 | RESEARCH | Counterfactual Simulator | Simulator fidelities and models | SRC-007 lines 4716–4718 | NO |
| REQ-PART-0017 | RESEARCH | Market Participants | Participant response model | SRC-007 lines 4719–4720 | NO |
| REQ-SURV-0013 | RESEARCH | Market Participants | Edge Survival | SRC-007 lines 4721–4725 | NO |
| REQ-EXEC-0261 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 4726–4733 | NO |
| REQ-XMARKET-0011 | RESEARCH | Market Participants | Cross-Market Response | SRC-007 lines 4734–4739 | NO |
| REQ-PART-0018 | RESEARCH | Market Participants | Participant response model | SRC-007 lines 4740–4744 | NO |
| REQ-SIM-0005 | RESEARCH | Counterfactual Simulator | Simulator fidelities and models | SRC-007 lines 4745–4754 | NO |
| REQ-ARCH-0078 | RESEARCH | Master Architecture | Architecture modules | SRC-007 lines 4755–4756 | NO |
| REQ-EXEC-0262 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 4757–4763 | NO |
| REQ-SURV-0014 | RESEARCH | Market Participants | Edge Survival | SRC-007 lines 4764–4766 | NO |
| REQ-LIQ-0005 | RESEARCH | Market Participants | Liquidity Response | SRC-007 lines 4767–4768 | NO |
| REQ-EXEC-0263 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 4769–4770 | NO |
| REQ-XMARKET-0012 | RESEARCH | Market Participants | Cross-Market Response | SRC-007 lines 4771–4772 | NO |
| REQ-PART-0019 | RESEARCH | Market Participants | Participant response model | SRC-007 lines 4773–4774 | NO |
| REQ-PART-0020 | FUTURE | Market Participants | Participant response model | SRC-007 lines 4775–4777 | NO |
| REQ-SURV-0015 | REJECTED | Market Participants | Edge Survival | SRC-007 lines 4778–4800 | NO |
| REQ-ACCT-0054 | FUTURE | Accounting | PnL attribution | SRC-007 lines 4801–4876 | NO |
| REQ-RISK-0302 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-007 lines 4877–4899 | NO |
| REQ-RISK-0303 | FUTURE | Risk Constitution | Risk gates and budgets | SRC-007 lines 4900–4931 | NO |
| REQ-RISK-0304 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-007 lines 4932–5138 | NO |
| REQ-EXEC-0264 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 5139–5188 | NO |
| REQ-EXEC-0265 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 5189–5206 | NO |
| REQ-ARCH-0079 | RESEARCH | Master Architecture | Architecture modules | SRC-007 lines 5207–5208 | NO |
| REQ-SURV-0016 | CALIBRATED | Market Participants | Edge Survival | SRC-007 lines 5209–5235 | NO |
| REQ-LIQ-0006 | RESEARCH | Market Participants | Liquidity Response | SRC-007 lines 5236–5269 | NO |
| REQ-XMARKET-0013 | RESEARCH | Market Participants | Cross-Market Response | SRC-007 lines 5270–5299 | NO |
| REQ-EXEC-0266 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 5300–5309 | NO |
| REQ-EXEC-0267 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 5310–5342 | NO |
| REQ-INFRA-0043 | LOCKED | Infrastructure Master | Infrastructure deep specs | SRC-007 lines 5343–5387 | NO |
| REQ-QUANT-0010 | LOCKED | Formula Book | Quant models | SRC-007 lines 5389–5448 | NO |
| REQ-QUANT-0011 | LOCKED | Formula Book | Quant models | SRC-007 lines 5449–5502 | NO |
| REQ-ARCH-0080 | RESEARCH | Master Architecture | Architecture modules | SRC-007 lines 5504–5514 | NO |
| REQ-RECOV-0017 | FUTURE | Execution State Machine | Recovery and Unknown State | SRC-007 lines 5515–5531 | NO |
| REQ-RISK-0305 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-007 lines 5532–5613 | NO |
| REQ-ACCT-0055 | RESEARCH | Accounting | PnL attribution | SRC-007 lines 5614–5668 | NO |
| REQ-QUANT-0012 | RESEARCH | Formula Book | Quant models | SRC-007 lines 5669–5676 | NO |
| REQ-MICRO-0011 | RESEARCH | Market Microstructure | OFI/MLOFI/queue | SRC-007 lines 5678–5683 | NO |
| REQ-FORMULA-0140 | RESEARCH | Formula Book | Formula audit/index | SRC-007 lines 5684–5731 | NO |
| REQ-RECOV-0018 | RESEARCH | Execution State Machine | Recovery and Unknown State | SRC-007 lines 5732–5742 | NO |
| REQ-ACCT-0056 | RESEARCH | Accounting | PnL attribution | SRC-007 lines 5743–5821 | NO |
| REQ-OWA-0005 | RESEARCH | Market Graph and Routes | OWA strategy | SRC-007 lines 5822–5834 | NO |
| REQ-ROUTE-0029 | RESEARCH | Market Graph and Routes | Route/NetConvert contracts | SRC-007 lines 5835–5860 | NO |
| REQ-ROUTE-0030 | RESEARCH | Market Graph and Routes | Route/NetConvert contracts | SRC-007 lines 5861–5908 | NO |
| REQ-OWA-0006 | RESEARCH | Market Graph and Routes | OWA strategy | SRC-007 lines 5909–5934 | NO |
| REQ-ARCH-0081 | RESEARCH | Master Architecture | Architecture modules | SRC-007 lines 5935–5958 | NO |
| REQ-OWA-0007 | LOCKED | Market Graph and Routes | OWA strategy | SRC-007 lines 5959–5980 | NO |
| REQ-RISK-0306 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-007 lines 5981–6030 | NO |
| REQ-RISK-0307 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-007 lines 6031–6083 | NO |
| REQ-TRI-0002 | RESEARCH | Market Graph and Routes | Triangle strategy | SRC-007 lines 6084–6213 | NO |
| REQ-EXEC-0268 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 6214–6286 | NO |
| REQ-RISK-0308 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-007 lines 6288–6298 | NO |
| REQ-EXEC-0269 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 6299–6399 | NO |
| REQ-EXEC-0270 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 6400–6480 | NO |
| REQ-EXEC-0271 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 6481–6514 | NO |
| REQ-PART-0021 | RESEARCH | Market Participants | Participant response model | SRC-007 lines 6516–6523 | NO |
| REQ-SURV-0017 | RESEARCH | Market Participants | Edge Survival | SRC-007 lines 6524–6556 | NO |
| REQ-SURV-0018 | LOCKED | Market Participants | Edge Survival | SRC-007 lines 6557–6577 | NO |
| REQ-SURV-0019 | RESEARCH | Market Participants | Edge Survival | SRC-007 lines 6578–6614 | NO |
| REQ-SURV-0020 | RESEARCH | Market Participants | Edge Survival | SRC-007 lines 6615–6643 | NO |
| REQ-INFRA-0044 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-007 lines 6644–6687 | NO |
| REQ-INFRA-0045 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-007 lines 6688–6717 | NO |
| REQ-BENCH-0007 | RESEARCH | Infrastructure Master | Benchmark Protocol | SRC-007 lines 6718–6757 | NO |
| REQ-FORMULA-0141 | RESEARCH | Formula Book | Formula audit/index | SRC-007 lines 6759–6805 | NO |
| REQ-EXEC-0272 | FUTURE | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 6806–6826 | NO |
| REQ-EXEC-0273 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 6828–6868 | NO |
| REQ-MICRO-0012 | CALIBRATED | Market Microstructure | OFI/MLOFI/queue | SRC-007 lines 6869–6926 | NO |
| REQ-MICRO-0013 | FUTURE | Market Microstructure | OFI/MLOFI/queue | SRC-007 lines 6927–6959 | NO |
| REQ-MICRO-0014 | EXTERNAL_REVALIDATION | Market Microstructure | OFI/MLOFI/queue | SRC-007 lines 6961–7021 | NO |
| REQ-MICRO-0015 | EXTERNAL_REVALIDATION | Market Microstructure | OFI/MLOFI/queue | SRC-007 lines 7022–7031 | NO |
| REQ-QUANT-0013 | RESEARCH | Formula Book | Quant models | SRC-007 lines 7033–7072 | NO |
| REQ-ACCT-0057 | CALIBRATED | Accounting | PnL attribution | SRC-007 lines 7073–7091 | NO |
| REQ-RECOV-0019 | RESEARCH | Execution State Machine | Recovery and Unknown State | SRC-007 lines 7092–7105 | NO |
| REQ-RISK-0309 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-007 lines 7106–7131 | NO |
| REQ-QUANT-0014 | RESEARCH | Formula Book | Quant models | SRC-007 lines 7132–7133 | NO |
| REQ-QUANT-0015 | RESEARCH | Formula Book | Quant models | SRC-007 lines 7134–7142 | NO |
| REQ-QUANT-0016 | RESEARCH | Formula Book | Quant models | SRC-007 lines 7143–7147 | NO |
| REQ-QUANT-0017 | RESEARCH | Formula Book | Quant models | SRC-007 lines 7148–7184 | NO |
| REQ-EXEC-0274 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 7185–7217 | NO |
| REQ-PRODUCT-0020 | LOCKED | Product and Scope | Product model | SRC-007 lines 7218–7236 | NO |
| REQ-LIQ-0007 | RESEARCH | Market Participants | Liquidity Response | SRC-007 lines 7237–7301 | NO |
| REQ-LIQ-0008 | RESEARCH | Market Participants | Liquidity Response | SRC-007 lines 7302–7325 | NO |
| REQ-SLICE-0004 | RESEARCH | Execution State Machine | Order Slicing | SRC-007 lines 7326–7416 | NO |
| REQ-EXEC-0275 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 7418–7449 | NO |
| REQ-EXEC-0276 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 7450–7493 | NO |
| REQ-MAKER-0001 | FUTURE | Market Participants | Maker fill and adverse selection | SRC-007 lines 7494–7544 | NO |
| REQ-EXEC-0277 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 7545–7673 | NO |
| REQ-RISK-0310 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-007 lines 7675–7699 | NO |
| REQ-RISK-0311 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-007 lines 7700–7712 | NO |
| REQ-RISK-0312 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-007 lines 7713–7740 | NO |
| REQ-RISK-0313 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-007 lines 7741–7773 | NO |
| REQ-ROUTE-0031 | RESEARCH | Market Graph and Routes | Route/NetConvert contracts | SRC-007 lines 7774–7793 | NO |
| REQ-EXEC-0278 | FUTURE | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 7795–7831 | NO |
| REQ-SIM-0006 | FUTURE | Counterfactual Simulator | Simulator fidelities and models | SRC-007 lines 7832–7887 | NO |
| REQ-SIM-0007 | RESEARCH | Counterfactual Simulator | Simulator fidelities and models | SRC-007 lines 7888–7907 | NO |
| REQ-RISK-0314 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-007 lines 7909–7942 | NO |
| REQ-SIZE-0003 | RESEARCH | Inventory and Capital | Position Sizing | SRC-007 lines 7943–8086 | NO |
| REQ-CAP-0018 | RESEARCH | Inventory and Capital | Capital reachability/capacity | SRC-007 lines 8087–8107 | NO |
| REQ-ACCT-0058 | RESEARCH | Accounting | PnL attribution | SRC-007 lines 8108–8132 | NO |
| REQ-PORT-0001 | RESEARCH | Inventory and Capital | Opportunity Portfolio | SRC-007 lines 8133–8148 | NO |
| REQ-RISK-0315 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-007 lines 8149–8267 | NO |
| REQ-EXEC-0279 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 8268–8283 | NO |
| REQ-INV-0020 | RESEARCH | Inventory and Capital | Inventory Engine | SRC-007 lines 8284–8378 | NO |
| REQ-INV-0021 | LOCKED | Inventory and Capital | Inventory Engine | SRC-007 lines 8379–8447 | NO |
| REQ-ARCH-0082 | CALIBRATED | Master Architecture | Architecture modules | SRC-007 lines 8448–8461 | NO |
| REQ-PORT-0002 | RESEARCH | Inventory and Capital | Opportunity Portfolio | SRC-007 lines 8462–8557 | NO |
| REQ-INV-0022 | RESEARCH | Inventory and Capital | Inventory Engine | SRC-007 lines 8558–8633 | NO |
| REQ-BRIDGE-0011 | RESEARCH | Inventory and Capital | Bridge/Relocation | SRC-007 lines 8634–8701 | NO |
| REQ-BRIDGE-0012 | RESEARCH | Inventory and Capital | Bridge/Relocation | SRC-007 lines 8702–8781 | NO |
| REQ-CAP-0019 | RESEARCH | Inventory and Capital | Capital reachability/capacity | SRC-007 lines 8782–8876 | NO |
| REQ-ACCT-0059 | RESEARCH | Accounting | PnL attribution | SRC-007 lines 8877–8917 | NO |
| REQ-PART-0022 | RESEARCH | Market Participants | Participant response model | SRC-007 lines 8919–8961 | NO |
| REQ-PART-0023 | RESEARCH | Market Participants | Participant response model | SRC-007 lines 8962–8974 | NO |
| REQ-QUANT-0018 | RESEARCH | Formula Book | Quant models | SRC-007 lines 8975–8988 | NO |
| REQ-QUANT-0019 | FUTURE | Formula Book | Quant models | SRC-007 lines 8990–9022 | NO |
| REQ-EXEC-0280 | CALIBRATED | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 9023–9034 | NO |
| REQ-QUANT-0020 | FUTURE | Formula Book | Quant models | SRC-007 lines 9035–9058 | NO |
| REQ-MICRO-0016 | FUTURE | Market Microstructure | OFI/MLOFI/queue | SRC-007 lines 9059–9103 | NO |
| REQ-ACCT-0060 | RESEARCH | Accounting | PnL attribution | SRC-007 lines 9104–9112 | NO |
| REQ-RISK-0316 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-007 lines 9113–9162 | NO |
| REQ-EXEC-0281 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 9163–9200 | NO |
| REQ-ARCH-0083 | RESEARCH | Master Architecture | Architecture modules | SRC-007 lines 9201–9242 | NO |
| REQ-FORMULA-0142 | CALIBRATED | Formula Book | Formula audit/index | SRC-007 lines 9243–9268 | NO |
| REQ-RISK-0317 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-007 lines 9269–9294 | NO |
| REQ-EXEC-0282 | FUTURE | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 9295–9316 | NO |
| REQ-PART-0024 | RESEARCH | Market Participants | Participant response model | SRC-007 lines 9317–9331 | NO |
| REQ-BENCH-0008 | LOCKED | Infrastructure Master | Benchmark Protocol | SRC-007 lines 9332–9355 | NO |
| REQ-INFRA-0046 | LOCKED | Infrastructure Master | Infrastructure deep specs | SRC-007 lines 9356–9398 | NO |
| REQ-INFRA-0047 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-007 lines 9399–9474 | NO |
| REQ-INFRA-0048 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-007 lines 9475–9541 | NO |
| REQ-INFRA-0049 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-007 lines 9542–9635 | NO |
| REQ-ACCT-0061 | RESEARCH | Accounting | PnL attribution | SRC-007 lines 9636–9654 | NO |
| REQ-SURV-0021 | RESEARCH | Market Participants | Edge Survival | SRC-007 lines 9655–9690 | NO |
| REQ-RISK-0318 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-007 lines 9691–9825 | NO |
| REQ-EXEC-0283 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 9826–9856 | NO |
| REQ-DATA-0319 | RESEARCH | Data Contracts | Schemas and event contracts | SRC-007 lines 9857–9881 | NO |
| REQ-MICRO-0017 | RESEARCH | Market Microstructure | OFI/MLOFI/queue | SRC-007 lines 9882–9905 | NO |
| REQ-FUTURE-0011 | FUTURE | Future Architecture | Future capability register | SRC-007 lines 9906–9917 | NO |
| REQ-INV-0023 | FUTURE | Inventory and Capital | Inventory Engine | SRC-007 lines 9918–9970 | NO |
| REQ-RECOV-0020 | RESEARCH | Execution State Machine | Recovery and Unknown State | SRC-007 lines 9971–10094 | NO |
| REQ-RECOV-0021 | FUTURE | Execution State Machine | Recovery and Unknown State | SRC-007 lines 10095–10131 | NO |
| REQ-ROUTE-0032 | FUTURE | Market Graph and Routes | Route/NetConvert contracts | SRC-007 lines 10132–10165 | NO |
| REQ-ROUTE-0033 | RESEARCH | Market Graph and Routes | Route/NetConvert contracts | SRC-007 lines 10166–10182 | NO |
| REQ-RISK-0319 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-007 lines 10183–10204 | NO |
| REQ-MICRO-0018 | RESEARCH | Market Microstructure | OFI/MLOFI/queue | SRC-007 lines 10205–10225 | NO |
| REQ-RISK-0320 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-007 lines 10226–10237 | NO |
| REQ-ARCH-0084 | CALIBRATED | Master Architecture | Architecture modules | SRC-007 lines 10238–10252 | NO |
| REQ-PRODUCT-0021 | RESEARCH | Product and Scope | Product model | SRC-007 lines 10253–10296 | NO |
| REQ-VALID-0371 | RESEARCH | Validation Matrix | M0–M5 evidence gates | SRC-007 lines 10297–10316 | NO |
| REQ-QUANT-0021 | EXTERNAL_REVALIDATION | Formula Book | Quant models | SRC-007 lines 10317–10334 | NO |
| REQ-RECOV-0022 | LOCKED | Execution State Machine | Recovery and Unknown State | SRC-007 lines 10335–10355 | NO |
| REQ-ROUTE-0034 | RESEARCH | Market Graph and Routes | Route/NetConvert contracts | SRC-007 lines 10356–10384 | NO |
| REQ-EXEC-0284 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 10385–10513 | NO |
| REQ-RISK-0321 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-007 lines 10514–10641 | NO |
| REQ-QUANT-0022 | RESEARCH | Formula Book | Quant models | SRC-007 lines 10642–10643 | NO |
| REQ-ROUTE-0035 | RESEARCH | Market Graph and Routes | Route/NetConvert contracts | SRC-007 lines 10644–10645 | NO |
| REQ-QUANT-0023 | RESEARCH | Formula Book | Quant models | SRC-007 lines 10646–10647 | NO |
| REQ-SURV-0022 | RESEARCH | Market Participants | Edge Survival | SRC-007 lines 10648–10649 | NO |
| REQ-MICRO-0019 | RESEARCH | Market Microstructure | OFI/MLOFI/queue | SRC-007 lines 10650–10651 | NO |
| REQ-RISK-0322 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-007 lines 10652–10653 | NO |
| REQ-EXEC-0285 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-007 lines 10654–10655 | NO |
| REQ-SIM-0008 | RESEARCH | Counterfactual Simulator | Simulator fidelities and models | SRC-007 lines 10656–10657 | NO |
| REQ-RISK-0323 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-007 lines 10658–10659 | NO |
| REQ-SIZE-0004 | RESEARCH | Inventory and Capital | Position Sizing | SRC-007 lines 10660–10661 | NO |
| REQ-PORT-0003 | RESEARCH | Inventory and Capital | Opportunity Portfolio | SRC-007 lines 10662–10664 | NO |
| REQ-QUANT-0024 | LOCKED | Formula Book | Quant models | SRC-007 lines 10665–10677 | NO |
| REQ-PORT-0004 | RESEARCH | Inventory and Capital | Opportunity Portfolio | SRC-007 lines 10678–10692 | NO |
| REQ-FORMULA-0143 | REJECTED | Formula Book | Formula audit/index | SRC-007 lines 10693–10717 | NO |
| REQ-QUANT-0025 | RESEARCH | Formula Book | Quant models | SRC-007 lines 10718–10806 | NO |
| REQ-QUANT-0026 | RESEARCH | Formula Book | Quant models | SRC-007 lines 10807–10879 | NO |
| REQ-RISK-0324 | FUTURE | Risk Constitution | Risk gates and budgets | SRC-007 lines 10880–10934 | NO |
| REQ-FORMULA-0144 | RESEARCH | Formula Book | Formula audit/index | SRC-007 lines 10935–11159 | NO |
| REQ-FORMULA-0145 | LOCKED | Formula Book | Formula audit/index | SRC-007 lines 11160–11210 | NO |
| REQ-FORMULA-0146 | RESEARCH | Formula Book | Formula audit/index | SRC-007 lines 11211–11724 | NO |
| REQ-FORMULA-0147 | CALIBRATED | Formula Book | Formula audit/index | SRC-007 lines 11725–11912 | NO |
| REQ-FORMULA-0148 | RESEARCH | Formula Book | Formula audit/index | SRC-007 lines 11913–12061 | NO |
| REQ-MICRO-0020 | EXTERNAL_REVALIDATION | Market Microstructure | OFI/MLOFI/queue | SRC-007 lines 12062–12119 | NO |
| REQ-FORMULA-0149 | RESEARCH | Formula Book | Formula audit/index | SRC-007 lines 12120–12204 | NO |
| REQ-FORMULA-0150 | CALIBRATED | Formula Book | Formula audit/index | SRC-007 lines 12205–12310 | NO |
| REQ-QUANT-0027 | RESEARCH | Formula Book | Quant models | SRC-007 lines 12311–12314 | NO |
| REQ-ACCT-0062 | RESEARCH | Accounting | PnL attribution | SRC-007 lines 12315–12324 | NO |
| REQ-MICRO-0021 | RESEARCH | Market Microstructure | OFI/MLOFI/queue | SRC-007 lines 12325–12336 | NO |
| REQ-QUANT-0028 | RESEARCH | Formula Book | Quant models | SRC-007 lines 12337–12345 | NO |
| REQ-RISK-0325 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-007 lines 12346–12350 | NO |
| REQ-INV-0024 | RESEARCH | Inventory and Capital | Inventory Engine | SRC-007 lines 12351–12356 | NO |
| REQ-INFRA-0050 | CALIBRATED | Infrastructure Master | Infrastructure deep specs | SRC-007 lines 12357–12371 | NO |
| REQ-QUANT-0029 | CALIBRATED | Formula Book | Quant models | SRC-008 lines 1–16 | NO |
| REQ-EXEC-0286 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 17–34 | NO |
| REQ-EXEC-0287 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 35–50 | NO |
| REQ-EXEC-0288 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 51–144 | NO |
| REQ-INFRA-0051 | LOCKED | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 145–170 | NO |
| REQ-EXEC-0289 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 171–214 | NO |
| REQ-TRI-0003 | RESEARCH | Market Graph and Routes | Triangle strategy | SRC-008 lines 215–260 | NO |
| REQ-VALID-0372 | RESEARCH | Validation Matrix | M0–M5 evidence gates | SRC-008 lines 261–281 | NO |
| REQ-VALID-0373 | FUTURE | Validation Matrix | M0–M5 evidence gates | SRC-008 lines 282–316 | NO |
| REQ-REPLAY-0018 | RESEARCH | Recorder and Replay | Replay engine | SRC-008 lines 317–329 | NO |
| REQ-EXEC-0290 | FUTURE | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 330–357 | NO |
| REQ-REPLAY-0019 | FUTURE | Recorder and Replay | Replay engine | SRC-008 lines 358–373 | NO |
| REQ-EXEC-0291 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 374–526 | NO |
| REQ-EXEC-0292 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 527–574 | NO |
| REQ-MICRO-0022 | RESEARCH | Market Microstructure | OFI/MLOFI/queue | SRC-008 lines 575–606 | NO |
| REQ-EXEC-0293 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 607–631 | NO |
| REQ-MICRO-0023 | EXTERNAL_REVALIDATION | Market Microstructure | OFI/MLOFI/queue | SRC-008 lines 632–727 | NO |
| REQ-QUANT-0030 | EXTERNAL_REVALIDATION | Formula Book | Quant models | SRC-008 lines 728–744 | NO |
| REQ-QUANT-0031 | RESEARCH | Formula Book | Quant models | SRC-008 lines 745–773 | NO |
| REQ-EXEC-0294 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 774–810 | NO |
| REQ-EXEC-0295 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 811–841 | NO |
| REQ-INFRA-0052 | FUTURE | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 842–857 | NO |
| REQ-EXEC-0296 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 858–876 | NO |
| REQ-EXEC-0297 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 877–905 | NO |
| REQ-ARCH-0085 | RESEARCH | Master Architecture | Architecture modules | SRC-008 lines 907–912 | NO |
| REQ-EXEC-0298 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 913–934 | NO |
| REQ-MICRO-0024 | RESEARCH | Market Microstructure | OFI/MLOFI/queue | SRC-008 lines 935–936 | NO |
| REQ-MICRO-0025 | RESEARCH | Market Microstructure | OFI/MLOFI/queue | SRC-008 lines 937–944 | NO |
| REQ-MICRO-0026 | RESEARCH | Market Microstructure | OFI/MLOFI/queue | SRC-008 lines 945–951 | NO |
| REQ-MICRO-0027 | RESEARCH | Market Microstructure | OFI/MLOFI/queue | SRC-008 lines 952–981 | NO |
| REQ-EXEC-0299 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 982–1003 | NO |
| REQ-EXEC-0300 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 1004–1019 | NO |
| REQ-EXEC-0301 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 1020–1070 | NO |
| REQ-MAKER-0002 | EXTERNAL_REVALIDATION | Market Participants | Maker fill and adverse selection | SRC-008 lines 1071–1093 | NO |
| REQ-EXEC-0302 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 1094–1106 | NO |
| REQ-EXEC-0303 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 1107–1133 | NO |
| REQ-EXEC-0304 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 1134–1163 | NO |
| REQ-XMARKET-0014 | RESEARCH | Market Participants | Cross-Market Response | SRC-008 lines 1164–1185 | NO |
| REQ-ROUTE-0036 | RESEARCH | Market Graph and Routes | Route/NetConvert contracts | SRC-008 lines 1186–1203 | NO |
| REQ-XMARKET-0015 | RESEARCH | Market Participants | Cross-Market Response | SRC-008 lines 1204–1250 | NO |
| REQ-XMARKET-0016 | RESEARCH | Market Participants | Cross-Market Response | SRC-008 lines 1251–1269 | NO |
| REQ-QUANT-0032 | RESEARCH | Formula Book | Quant models | SRC-008 lines 1270–1292 | NO |
| REQ-EXEC-0305 | FUTURE | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 1293–1321 | NO |
| REQ-EXEC-0306 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 1322–1348 | NO |
| REQ-RISK-0326 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-008 lines 1349–1350 | NO |
| REQ-ARCH-0086 | RESEARCH | Master Architecture | Architecture modules | SRC-008 lines 1351–1357 | NO |
| REQ-RECOV-0023 | RESEARCH | Execution State Machine | Recovery and Unknown State | SRC-008 lines 1358–1376 | NO |
| REQ-INFRA-0053 | LOCKED | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 1377–1392 | NO |
| REQ-PRODUCT-0022 | LOCKED | Product and Scope | Product model | SRC-008 lines 1393–1425 | NO |
| REQ-RISK-0327 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-008 lines 1426–1444 | NO |
| REQ-CAP-0020 | CALIBRATED | Inventory and Capital | Capital reachability/capacity | SRC-008 lines 1445–1484 | NO |
| REQ-EXEC-0307 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 1485–1507 | NO |
| REQ-SLICE-0005 | RESEARCH | Execution State Machine | Order Slicing | SRC-008 lines 1508–1509 | NO |
| REQ-ARCH-0087 | RESEARCH | Master Architecture | Architecture modules | SRC-008 lines 1510–1514 | NO |
| REQ-ARCH-0088 | RESEARCH | Master Architecture | Architecture modules | SRC-008 lines 1515–1520 | NO |
| REQ-ARCH-0089 | RESEARCH | Master Architecture | Architecture modules | SRC-008 lines 1521–1526 | NO |
| REQ-ARCH-0090 | RESEARCH | Master Architecture | Architecture modules | SRC-008 lines 1527–1536 | NO |
| REQ-QUANT-0033 | RESEARCH | Formula Book | Quant models | SRC-008 lines 1537–1550 | NO |
| REQ-SLICE-0006 | FUTURE | Execution State Machine | Order Slicing | SRC-008 lines 1551–1609 | NO |
| REQ-QUANT-0034 | EXTERNAL_REVALIDATION | Formula Book | Quant models | SRC-008 lines 1610–1621 | NO |
| REQ-SIM-0009 | FUTURE | Counterfactual Simulator | Simulator fidelities and models | SRC-008 lines 1622–1672 | NO |
| REQ-EXEC-0308 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 1673–1686 | NO |
| REQ-EXEC-0309 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 1687–1694 | NO |
| REQ-EXEC-0310 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 1695–1730 | NO |
| REQ-RECOV-0024 | RESEARCH | Execution State Machine | Recovery and Unknown State | SRC-008 lines 1731–1750 | NO |
| REQ-LIQ-0009 | LOCKED | Market Participants | Liquidity Response | SRC-008 lines 1751–1768 | NO |
| REQ-SIM-0010 | EXTERNAL_REVALIDATION | Counterfactual Simulator | Simulator fidelities and models | SRC-008 lines 1769–1784 | NO |
| REQ-PART-0025 | EXTERNAL_REVALIDATION | Market Participants | Participant response model | SRC-008 lines 1785–1798 | NO |
| REQ-EXEC-0311 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 1799–1821 | NO |
| REQ-ARCH-0091 | RESEARCH | Master Architecture | Architecture modules | SRC-008 lines 1822–1885 | NO |
| REQ-PRODUCT-0023 | FUTURE | Product and Scope | Product model | SRC-008 lines 1886–1888 | NO |
| REQ-ACCT-0063 | RESEARCH | Accounting | PnL attribution | SRC-008 lines 1889–1897 | NO |
| REQ-INFRA-0054 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 1898–1910 | NO |
| REQ-MICRO-0028 | RESEARCH | Market Microstructure | OFI/MLOFI/queue | SRC-008 lines 1911–1923 | NO |
| REQ-LIQ-0010 | RESEARCH | Market Participants | Liquidity Response | SRC-008 lines 1924–1936 | NO |
| REQ-SIM-0011 | RESEARCH | Counterfactual Simulator | Simulator fidelities and models | SRC-008 lines 1937–1950 | NO |
| REQ-EXEC-0312 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 1951–1985 | NO |
| REQ-EXEC-0313 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 1986–2009 | NO |
| REQ-VALID-0374 | RESEARCH | Validation Matrix | M0–M5 evidence gates | SRC-008 lines 2010–2022 | NO |
| REQ-VALID-0375 | RESEARCH | Validation Matrix | M0–M5 evidence gates | SRC-008 lines 2023–2054 | NO |
| REQ-EXEC-0314 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 2055–2071 | NO |
| REQ-VALID-0376 | RESEARCH | Validation Matrix | M0–M5 evidence gates | SRC-008 lines 2072–2128 | NO |
| REQ-VALID-0377 | RESEARCH | Validation Matrix | M0–M5 evidence gates | SRC-008 lines 2129–2143 | NO |
| REQ-FUTURE-0012 | FUTURE | Future Architecture | Future capability register | SRC-008 lines 2144–2167 | NO |
| REQ-ARCH-0092 | RESEARCH | Master Architecture | Architecture modules | SRC-008 lines 2168–2169 | NO |
| REQ-ARCH-0093 | RESEARCH | Master Architecture | Architecture modules | SRC-008 lines 2170–2173 | NO |
| REQ-ARCH-0094 | RESEARCH | Master Architecture | Architecture modules | SRC-008 lines 2174–2182 | NO |
| REQ-PART-0026 | RESEARCH | Market Participants | Participant response model | SRC-008 lines 2183–2186 | NO |
| REQ-EXEC-0315 | FUTURE | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 2187–2200 | NO |
| REQ-EXEC-0316 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 2201–2219 | NO |
| REQ-EXEC-0317 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 2220–2262 | NO |
| REQ-EXEC-0318 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 2263–2313 | NO |
| REQ-ROUTE-0037 | RESEARCH | Market Graph and Routes | Route/NetConvert contracts | SRC-008 lines 2314–2351 | NO |
| REQ-SIZE-0005 | RESEARCH | Inventory and Capital | Position Sizing | SRC-008 lines 2352–2431 | NO |
| REQ-EXEC-0319 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 2433–2445 | NO |
| REQ-EXEC-0320 | FUTURE | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 2446–2463 | NO |
| REQ-FORMULA-0151 | FUTURE | Formula Book | Formula audit/index | SRC-008 lines 2464–2564 | NO |
| REQ-EXEC-0321 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 2565–2620 | NO |
| REQ-EXEC-0322 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 2621–2640 | NO |
| REQ-EXEC-0323 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 2641–2663 | NO |
| REQ-EXEC-0324 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 2664–2706 | NO |
| REQ-EXEC-0325 | FUTURE | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 2707–2748 | NO |
| REQ-EXEC-0326 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 2749–2775 | NO |
| REQ-OWA-0008 | LOCKED | Market Graph and Routes | OWA strategy | SRC-008 lines 2776–2826 | NO |
| REQ-EXEC-0327 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 2827–2861 | NO |
| REQ-INFRA-0055 | LOCKED | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 2863–2928 | NO |
| REQ-EXEC-0328 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 2929–3185 | NO |
| REQ-INFRA-0056 | CALIBRATED | Infrastructure Master | 01 Baseline and Deployment Profiles | SRC-008 lines 3186–3205 | NO |
| REQ-INFRA-0057 | LOCKED | Infrastructure Master | 06 Node, Feed and Scale Gates | SRC-008 lines 3206–3238 | NO |
| REQ-INFRA-0058 | CALIBRATED | Infrastructure Master | 01 Baseline and Deployment Profiles | SRC-008 lines 3239–3276 | NO |
| REQ-INFRA-0059 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 3277–3308 | NO |
| REQ-INFRA-0060 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 3309–3339 | NO |
| REQ-INFRA-0061 | SOURCE_SNAPSHOT | Infrastructure Master | 02 Provider Candidates | SRC-008 lines 3341–3370 | NO |
| REQ-INFRA-0062 | SOURCE_SNAPSHOT | Infrastructure Master | 02 Provider Candidates | SRC-008 lines 3371–3463 | NO |
| REQ-INFRA-0063 | SOURCE_SNAPSHOT | Infrastructure Master | 02 Provider Candidates | SRC-008 lines 3464–3482 | NO |
| REQ-INFRA-0064 | SOURCE_SNAPSHOT | Infrastructure Master | 02 Provider Candidates | SRC-008 lines 3483–3502 | NO |
| REQ-INFRA-0065 | SOURCE_SNAPSHOT | Infrastructure Master | 02 Provider Candidates | SRC-008 lines 3503–3528 | NO |
| REQ-INFRA-0066 | SOURCE_SNAPSHOT | Infrastructure Master | 02 Provider Candidates | SRC-008 lines 3529–3542 | NO |
| REQ-INFRA-0067 | SOURCE_SNAPSHOT | Infrastructure Master | 02 Provider Candidates | SRC-008 lines 3543–3557 | NO |
| REQ-INFRA-0068 | SOURCE_SNAPSHOT | Infrastructure Master | 02 Provider Candidates | SRC-008 lines 3558–3583 | NO |
| REQ-INFRA-0069 | SOURCE_SNAPSHOT | Infrastructure Master | 02 Provider Candidates | SRC-008 lines 3584–3610 | NO |
| REQ-BENCH-0009 | LOCKED | Infrastructure Master | Benchmark Protocol | SRC-008 lines 3611–3632 | NO |
| REQ-INFRA-0070 | EXTERNAL_REVALIDATION | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 3633–3659 | NO |
| REQ-BENCH-0010 | LOCKED | Infrastructure Master | Benchmark Protocol | SRC-008 lines 3660–3682 | NO |
| REQ-ARCH-0095 | RESEARCH | Master Architecture | Architecture modules | SRC-008 lines 3684–3691 | NO |
| REQ-RISK-0328 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-008 lines 3692–3710 | NO |
| REQ-CLOCK-0015 | RESEARCH | Data Contracts | Clock and RNG contract | SRC-008 lines 3711–3769 | NO |
| REQ-BENCH-0011 | EXTERNAL_REVALIDATION | Infrastructure Master | Benchmark Protocol | SRC-008 lines 3770–3846 | NO |
| REQ-BENCH-0012 | RESEARCH | Infrastructure Master | Benchmark Protocol | SRC-008 lines 3847–3889 | NO |
| REQ-BENCH-0013 | RESEARCH | Infrastructure Master | Benchmark Protocol | SRC-008 lines 3890–3915 | NO |
| REQ-BENCH-0014 | LOCKED | Infrastructure Master | Benchmark Protocol | SRC-008 lines 3916–3947 | NO |
| REQ-BENCH-0015 | RESEARCH | Infrastructure Master | Benchmark Protocol | SRC-008 lines 3948–3967 | NO |
| REQ-INFRA-0071 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 3968–4005 | NO |
| REQ-INFRA-0072 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 4006–4075 | NO |
| REQ-INFRA-0073 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 4076–4093 | NO |
| REQ-EXEC-0329 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 4094–4181 | NO |
| REQ-BENCH-0016 | LOCKED | Infrastructure Master | Benchmark Protocol | SRC-008 lines 4182–4195 | NO |
| REQ-INFRA-0074 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 4196–4227 | NO |
| REQ-BENCH-0017 | RESEARCH | Infrastructure Master | Benchmark Protocol | SRC-008 lines 4228–4230 | NO |
| REQ-ARCH-0096 | RESEARCH | Master Architecture | Architecture modules | SRC-008 lines 4231–4235 | NO |
| REQ-DEPLOY-0217 | LOCKED | Deployment and Docker | Client deployment lifecycle | SRC-008 lines 4236–4250 | NO |
| REQ-ARCH-0097 | RESEARCH | Master Architecture | Architecture modules | SRC-008 lines 4251–4377 | NO |
| REQ-EXEC-0330 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 4378–4412 | NO |
| REQ-VALID-0378 | RESEARCH | Validation Matrix | M0–M5 evidence gates | SRC-008 lines 4413–4442 | NO |
| REQ-INFRA-0075 | EXTERNAL_REVALIDATION | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 4443–4456 | NO |
| REQ-INFRA-0076 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 4457–4574 | NO |
| REQ-SURV-0023 | RESEARCH | Market Participants | Edge Survival | SRC-008 lines 4575–4649 | NO |
| REQ-INFRA-0077 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 4650–4681 | NO |
| REQ-EXEC-0331 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 4682–4705 | NO |
| REQ-INFRA-0078 | FUTURE | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 4706–4739 | NO |
| REQ-INFRA-0079 | FUTURE | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 4740–4810 | NO |
| REQ-ACCT-0064 | RESEARCH | Accounting | PnL attribution | SRC-008 lines 4811–4859 | NO |
| REQ-ACCT-0065 | EXTERNAL_REVALIDATION | Accounting | PnL attribution | SRC-008 lines 4860–4908 | NO |
| REQ-INFRA-0080 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 4909–4924 | NO |
| REQ-ACCT-0066 | RESEARCH | Accounting | PnL attribution | SRC-008 lines 4925–4951 | NO |
| REQ-INFRA-0081 | FUTURE | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 4952–5008 | NO |
| REQ-INFRA-0082 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 5009–5051 | NO |
| REQ-ACCT-0067 | RESEARCH | Accounting | PnL attribution | SRC-008 lines 5052–5168 | NO |
| REQ-INFRA-0083 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 5170–5177 | NO |
| REQ-INFRA-0084 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 5178–5198 | NO |
| REQ-INFRA-0085 | CALIBRATED | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 5199–5229 | NO |
| REQ-INFRA-0086 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 5230–5272 | NO |
| REQ-INFRA-0087 | LOCKED | Infrastructure Master | 05 Infrastructure Economics and ROI | SRC-008 lines 5273–5298 | NO |
| REQ-CAP-0021 | LOCKED | Inventory and Capital | Capital reachability/capacity | SRC-008 lines 5299–5356 | NO |
| REQ-CAP-0022 | RESEARCH | Inventory and Capital | Capital reachability/capacity | SRC-008 lines 5357–5385 | NO |
| REQ-NODE-0003 | EXTERNAL_REVALIDATION | Infrastructure Master | Node Feed and Scale Gates | SRC-008 lines 5386–5471 | NO |
| REQ-INFRA-0088 | EXTERNAL_REVALIDATION | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 5472–5492 | NO |
| REQ-INFRA-0089 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 5493–5517 | NO |
| REQ-ROUTE-0038 | LOCKED | Market Graph and Routes | Route/NetConvert contracts | SRC-008 lines 5518–5557 | NO |
| REQ-INFRA-0090 | EXTERNAL_REVALIDATION | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 5558–5587 | NO |
| REQ-INFRA-0091 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 5588–5614 | NO |
| REQ-INFRA-0092 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 5615–5690 | NO |
| REQ-EXEC-0332 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 5691–5726 | NO |
| REQ-BENCH-0018 | EXTERNAL_REVALIDATION | Infrastructure Master | Benchmark Protocol | SRC-008 lines 5727–5768 | NO |
| REQ-BENCH-0019 | EXTERNAL_REVALIDATION | Infrastructure Master | Benchmark Protocol | SRC-008 lines 5769–5798 | NO |
| REQ-MICRO-0029 | RESEARCH | Market Microstructure | OFI/MLOFI/queue | SRC-008 lines 5799–5823 | NO |
| REQ-EXEC-0333 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 5824–5833 | NO |
| REQ-EXEC-0334 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 5834–5859 | NO |
| REQ-CLIENT-0025 | RESEARCH | Product and Deployment | Client distribution model | SRC-008 lines 5860–5891 | NO |
| REQ-DEPLOY-0218 | FUTURE | Deployment and Docker | Client deployment lifecycle | SRC-008 lines 5892–5908 | NO |
| REQ-CLIENT-0026 | RESEARCH | Product and Deployment | Client distribution model | SRC-008 lines 5909–5932 | NO |
| REQ-DEPLOY-0219 | EXTERNAL_REVALIDATION | Deployment and Docker | Client deployment lifecycle | SRC-008 lines 5933–5947 | NO |
| REQ-SEC-0021 | RESEARCH | Deployment and Security | Security baseline | SRC-008 lines 5948–5965 | NO |
| REQ-ROUTE-0039 | FUTURE | Market Graph and Routes | Route/NetConvert contracts | SRC-008 lines 5966–5989 | NO |
| REQ-CLIENT-0027 | LOCKED | Product and Deployment | Client distribution model | SRC-008 lines 5990–6011 | NO |
| REQ-CLIENT-0028 | RESEARCH | Product and Deployment | Client distribution model | SRC-008 lines 6012–6013 | NO |
| REQ-INFRA-0093 | FUTURE | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 6014–6021 | NO |
| REQ-INFRA-0094 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 6022–6028 | NO |
| REQ-BENCH-0020 | RESEARCH | Infrastructure Master | Benchmark Protocol | SRC-008 lines 6029–6037 | NO |
| REQ-INFRA-0095 | LOCKED | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 6038–6061 | NO |
| REQ-OPS-0019 | RESEARCH | Operations and Monitoring | Failure/recovery runbooks | SRC-008 lines 6062–6094 | NO |
| REQ-OPS-0020 | FUTURE | Operations and Monitoring | Failure/recovery runbooks | SRC-008 lines 6095–6113 | NO |
| REQ-RISK-0329 | LOCKED | Risk Constitution | Risk gates and budgets | SRC-008 lines 6114–6139 | NO |
| REQ-INFRA-0096 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 6140–6166 | NO |
| REQ-EXEC-0335 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 6167–6200 | NO |
| REQ-RISK-0330 | RESEARCH | Risk Constitution | Risk gates and budgets | SRC-008 lines 6201–6224 | NO |
| REQ-INFRA-0097 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 6225–6241 | NO |
| REQ-EXEC-0336 | LOCKED | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 6242–6288 | NO |
| REQ-INFRA-0098 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 6289–6321 | NO |
| REQ-REPLAY-0020 | FUTURE | Recorder and Replay | Replay engine | SRC-008 lines 6322–6361 | NO |
| REQ-SIZE-0006 | RESEARCH | Inventory and Capital | Position Sizing | SRC-008 lines 6362–6393 | NO |
| REQ-EXEC-0337 | RESEARCH | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 6394–6395 | NO |
| REQ-TRI-0004 | RESEARCH | Market Graph and Routes | Triangle strategy | SRC-008 lines 6396–6403 | NO |
| REQ-TRI-0005 | LOCKED | Market Graph and Routes | Triangle strategy | SRC-008 lines 6404–6421 | NO |
| REQ-RISK-0331 | EXTERNAL_REVALIDATION | Risk Constitution | Risk gates and budgets | SRC-008 lines 6422–6438 | NO |
| REQ-EXEC-0338 | FUTURE | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 6439–6453 | NO |
| REQ-OPS-0021 | OPEN | Operations and Monitoring | Failure/recovery runbooks | SRC-008 lines 6454–6499 | NO |
| REQ-INFRA-0099 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 6500–6545 | NO |
| REQ-OPS-0022 | EXTERNAL_REVALIDATION | Operations and Monitoring | Failure/recovery runbooks | SRC-008 lines 6546–6628 | NO |
| REQ-OPS-0023 | RESEARCH | Operations and Monitoring | Failure/recovery runbooks | SRC-008 lines 6629–6645 | NO |
| REQ-BENCH-0021 | RESEARCH | Infrastructure Master | Benchmark Protocol | SRC-008 lines 6646–6660 | NO |
| REQ-INFRA-0100 | RESEARCH | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 6662–6671 | NO |
| REQ-INFRA-0101 | EXTERNAL_REVALIDATION | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 6672–6680 | NO |
| REQ-FUTURE-0013 | FUTURE | Future Architecture | Future capability register | SRC-008 lines 6681–6689 | NO |
| REQ-DEPLOY-0220 | REJECTED | Deployment and Docker | Client deployment lifecycle | SRC-008 lines 6690–6725 | NO |
| REQ-EXEC-0339 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 6726–6779 | NO |
| REQ-INFRA-0102 | LOCKED | Infrastructure Master | Infrastructure deep specs | SRC-008 lines 6780–6879 | NO |
| REQ-EXEC-0340 | EXTERNAL_REVALIDATION | Execution State Machine | Order/Fill/Cancel contracts | SRC-008 lines 6880–6937 | NO |
| REQ-OWA-9001 | RESEARCH | Market Graph and Routes | OWA and Bridge classification | SRC-003 lines 2562–2615; SRC-004 QF-016–QF-020 | NO |
| REQ-SIZE-9001 | LOCKED | Inventory and Capital | Position Sizing | SRC-004 QF-075/QF-076; SRC-006/SRC-007 | NO |
| REQ-SLICE-9001 | LOCKED | Execution State Machine | Order Slicing | SRC-007 lines 7326–7416; SRC-004 QF-041 | NO |
| REQ-FORMULA-9001 | LOCKED | Formula Book | Alpha decomposition | SRC-004 QF-024 | NO |
| REQ-FORMULA-9002 | LOCKED | Formula Book | Alpha decomposition | SRC-004 QF-025 | NO |
| REQ-EXEC-9001 | LOCKED | Execution State Machine | Expected/Actual reconciliation | SRC-004/SRC-005 | NO |
| REQ-RISK-9001 | LOCKED | Risk Constitution | Unknown-state policy | SRC-004/SRC-005/SRC-006 | NO |
| REQ-REPLAY-9001 | LOCKED | Data and Replay | Replay/Live parity | SRC-005 lines 5374–5405 and 9762–9877 | NO |
| REQ-DET-9001 | LOCKED | Data Contracts | Determinism and parity | SRC-005 lines 5376–5410, 7033–7079 and 9668–9699 | NO |
| REQ-SIM-9001 | RESEARCH | Counterfactual Simulator | Simulator fidelity and calibration | SRC-008 lines 1–18; SRC-007 lines 3000–3072 | NO |
| REQ-PART-9001 | RESEARCH | Market Participants | Participant response model | SRC-007/SRC-008 | NO |
| REQ-INFRA-9001 | LOCKED | Infrastructure Master | Infrastructure ROI and downgrade | SRC-004 QF-087–QF-093; SRC-008 lines 6726–6937 | NO |
| REQ-CLIENT-9001 | LOCKED | Product and Deployment | Client distribution model | SRC-006 lines 5–40 and 1562–1573; SRC-008 lines 6715–6779 | NO |

## PASS 01 — Infrastructure target overlay

The authoritative per-requirement PASS 01 routing for all 514 reviewed Infrastructure requirements is `pass01_infrastructure/INFRA_REQUIREMENT_LEDGER.md`. Infrastructure-owned material targets `13_INFRASTRUCTURE.md` and one of the seven deep specs. Cross-domain requirements retain their future domain master as primary destination and are recorded as `REVIEWED_DEPENDENCY`; no primary ownership was silently moved.

## PASS 03 — Counterfactual Simulator target overlay

The authoritative normalized per-requirement routing for all 231 Simulator-index requirements and 42 checked QF dependencies is `pass03_simulator/SIMULATOR_REQUIREMENT_LEDGER.md`. Simulator-owned material targets `07_COUNTERFACTUAL_SIMULATOR.md` and `deep-specs/simulator/01..12`. Formula, Data/Replay, Risk, Execution/Recovery, Participant, Sizing and Graph requirements preserve their owning future-pass target while their Simulator-facing contract is cross-linked. Destinationless requirements: 0; primary ownership moved silently: 0.

## PASS 04 — Execution target overlay

The authoritative normalized routing for all **865** Execution-index requirements is `pass04_execution/EXECUTION_REQUIREMENT_LEDGER.md`. Closure-owned requirements target `10_EXECUTION_STATE_MACHINE.md` and `deep-specs/execution/01..12`; Risk, Data/Replay, Inventory/Sizing/Capital, Routing/Graph, Participants, Infrastructure, Operations, Validation, Security/Deployment and Formula retain their owning passes. External facts also target `EXTERNAL_REVALIDATION_REGISTER.md`. Destinationless requirements: **0**; silently moved primary ownership: **0**; stable IDs renumbered: **0**.

## PASS 05 — Risk target overlay

The authoritative normalized routing for all **752** Risk-index requirements is `pass05_risk/RISK_REQUIREMENT_LEDGER.md`. SRC-005 Dossier 3/6 closure material targets `09_RISK_CONSTITUTION.md` and `deep-specs/risk/01..11`; supporting Risk items target those deep specs. Formula, Data/Replay, Execution/Recovery, Inventory/Sizing/Capital/Portfolio, Routing/Graph, Participants/Simulator, Infrastructure, Operations, Validation, Security/Deployment and Product retain their owning passes. External facts also target `EXTERNAL_REVALIDATION_REGISTER.md`. Destinationless requirements: **0**; silently moved primary ownership: **0**; stable IDs renumbered: **0**.
