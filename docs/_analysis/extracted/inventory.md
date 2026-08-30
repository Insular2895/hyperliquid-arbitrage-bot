# Extraction — inventaire et capital

## Sources

SRC-002/SRC-003; SRC-004 QF-064..080/105..110 et SRC-005 Risk priment.

## Contrats retenus

- `CORE_INVENTORY`, `TRANSIT`, `EXCLUDED` selon données Hyperliquid, jamais par
  intuition statique.
- Target/soft/hard bands et net flows; soft penalty calibrée, hard gate
  infranchissable par nouveau risque.
- `Actual`, `Available`, `Reserved`, `Pending/Unknown` par AssetLocation;
  available nonnegative et unknown reserved.
- Terminal Viability vérifie exits/depth/cost/idle/volatility/opportunity/stranded.
- ConversionAlpha, relocation, route/recovery/rebalance PnL, inventory MTM et
  EconomicPnL restent séparés.
- Bridge paths comparés par NetConvert et QF-068..072; hystérésis/cooldown.
- Recovery optimise depuis l'état courant, sunk costs exclus, split permis.
- Cross-venue prefunded inventory/rebalancing reste future et exige ADR.
