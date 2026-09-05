# 08 — Simulator Fidelity and Calibration Validation

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

F0 historical/exogenous, F1 latency/mechanical, F2 local ShadowBook intervention, F3 learned stochastic response and F4 explicit-agent research are separate fidelity claims. Availability of F3/F4 code does not validate their use.

Mechanical validation covers arrival reconstruction, directed L2 walk, fee/precision rules, partial/zero/reject/cancel and Recovery. State/branch conservation, RNG repeatability, branch horizon/rejoin and cross-market inputs have properties and golden fixtures.

F3 requires temporal OOS response evidence and predicted/actual Micro-live comparison for fill, time, slippage, depth/spread/price/replenishment, Recovery and PnL distributions. Evaluate calibration, coverage, sharpness, tails and OOD/support by slice. The output is a distribution of plausible outcomes, not the exact alternate world.

F4 is a challenger/stress laboratory. Stylized realism or scale of synthetic agents cannot make it production truth. Persistent live underestimation lowers Simulator confidence/Q_validated and can disable dependent modes until revalidated.
