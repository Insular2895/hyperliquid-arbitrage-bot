# Bridge Decision Pipeline

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

```text
CURRENT CAPITAL STATE
        |
POINT-IN-TIME CURRENT / FORECAST MARKET ATLAS
        |
CANDIDATE DESTINATIONS (including STAY)
        |
ALLOWED CANDIDATE PATHS
        |
QF-070 BRIDGE COST via QF-016 NETCONVERT
        |
QF-068 EXPECTED EXIT COST
        |
RELOCATION RISK COST
        |
EV_destination versus EV_stay
        |
QF-072 CAPITAL RELOCATION VALUE
        |
PERSISTENCE + HYSTERESIS + COOLDOWN
        |
PASS05 RISK ELIGIBILITY
        |
SHARED BALANCE / BOOK / RISK RESERVATION
        |
PASS04 EXECUTION
        |
ACTUAL FILL-DERIVED CAPITAL STATE
        |
OUTCOME / STAY COUNTERFACTUAL / CALIBRATION
```

The source locks economic comparison, Risk, STAY and anti-flip-flop structure. Thresholds, horizons and cooldown are calibrated. PASS08 supplies routes/Atlas and may refine the exact interface without changing this ownership boundary.
