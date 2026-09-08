# Speculative Input Lane Contract

`STATUS: RESEARCH — NON-CANONICAL — NO CAPITAL AUTHORITY`

Speculative input is information received before it is authoritative enough to mutate canonical economic state. It may be predictive without being committed. It uses a separate typed representation such as `SpeculativeMarketEvent`, `SpeculativeMarketState`, `SpeculativeOpportunity` and `SpeculativeForecast`; none aliases canonical IDs or types.

## Allowed initially

Decode; normalize with speculative provenance; identify markets/routes; prefetch static metadata; warm caches/buffers; perform tentative BBO/route lookup/economics; prepare pure reusable computation; produce research forecasts; and record evidence.

## Forbidden initially

Canonical Book/Account/Order mutation; Fill application; Inventory or Reservation mutation; realized PnL; completion, Recovery or Reconciliation transition; canonical Opportunity count; Risk-increasing authorization; pre-signing or sending an order solely from speculative state.

Only canonical arrival may trigger normal validation. Speculative input cannot make the system more active during feed degradation. Status remains Research through M0–M3; any future real-send influence requires a new explicit human/Risk design before M4.
