# Market Liquidity, Volatility and Impact Risk

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

## Ordered market gates

After hard eligibility, market evaluation covers spread, executable liquidity, depth participation, volume participation, mechanical impact, jump state and realized volatility. Exact equations remain Formula Book authority (`QF-002`–`QF-006`, `QF-038`–`QF-042`).

| Gate | Hard structure | Calibrated/learned value |
|---|---|---|
| `SpreadGate` | Unsupported/excessive spread cannot be ignored. | Maximum spread/economic support by market/regime. |
| `LiquidityGate` | Quantity must be supported by executable depth. | Minimum depth, levels/bands and safety margin. |
| `DepthParticipationGate` | Proposed use must stay within validated depth share. | Maximum share by market/regime/side. |
| `VolumeParticipationGate` | Size cannot dominate recent supported volume. | Window and maximum participation. |
| `ImpactGate` | Mechanical impact/protected price must be acceptable. | Maximum impact/slippage and model margin. |
| `VolatilityGate` | Unsupported volatility tightens or rejects. | Estimator window and state thresholds. |
| `JumpGate` | Abnormal jump state triggers stricter policy. | Robust score window/threshold and hysteresis. |

An action may be reduced only when the reduced size passes every hard condition. A high expected edge cannot compensate for bad data, unsupported impact or an exceeded tail bound.

## Suspicious opportunities

When an edge is far beyond validated support, Risk checks sequence/freshness, cross-market consistency, metadata, fee/precision state and model support; it lowers confidence, may require a fresh snapshot and may reject. “Too good to be true” is a data/model risk pattern, not an alpha multiplier.

## Capacity boundary

Visible depth is not validated capacity. Sizing intersects book capacity, market participation, impact, model support, inventory, tail and execution evidence. Low liquidity cannot be made safe by faster infrastructure, and shared depth cannot be counted by more than one plan.

Source: SRC-005 lines 1033–1272, 2900–2984 and 4942–4970.
