# Asset Classification Matrix

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

Frozen Data enum: `CoreInventory`, `Transit`, `Excluded`. Economic labels below preserve source vocabulary. Classification values are learned/versioned; no example asset is pre-classified.

| Class | Purpose | Intentionally accumulated? | Target | Soft band | Hard band | Terminal acceptable? | Bridge destination? | Recovery destination? | Required exit | Capital utility | Risk implication | Reclassification | Source |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| `CORE_INVENTORY` | Normal bounded capital residence | Yes, inside validated bands | Required | Required | Required | Yes if Terminal Viability passes | Yes | Yes if safe/best exit | Credible size-aware exit | Empirically positive/supported | concentration, hard/soft, exit and model gates | Versioned evidence + hysteresis/persistence | SRC-003 §§20–29; SRC-005 §§62–74/Data §37 |
| `TRANSIT` | Temporary path intermediate | No normal accumulation | Normally low/residual policy | Tight/calibrated | Age/value Risk bounds | No normal terminal | No, unless controlled reclassification | Yes as intermediate exit if safest | Immediate credible continuation/recovery | Transitional only | short age/value; excess triggers Rebalance/Recovery | Evidence-backed promotion/demotion only | SRC-003 §22; SRC-005 §69 |
| `EXCLUDED` | Unsupported/unsafe asset | No | None | None | No new intentional exposure | No | No | Only to reduce existing accidental exposure | Best safe exit for existing exposure | None for new risk | reject intentional use | Requires new validated evidence and governed class change | SRC-003 §23; SRC-005 Risk |

No additional canonical category was found. Venue/location is a separate state dimension, not a fourth asset class.
