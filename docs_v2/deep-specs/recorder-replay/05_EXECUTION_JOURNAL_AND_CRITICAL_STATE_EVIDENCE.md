# Execution Journal and Critical-state Evidence

DOCUMENTATION STATUS:
REBUILD IN PROGRESS

ExecutionJournal is append-only, ordered independently by `journal_seq`, timestamped and optionally per-record/checkpoint checksummed. Its minimum closure events are `ExecutionCreated`, `ReservationCreated`, `OrderIntentCreated`, `OrderSent`, `FillApplied`, `CancelRequested`, `RecoveryStarted`, and `ExecutionCompleted`; PASS 04 expands the state-machine event vocabulary.

Journal evidence preserves commands/intents and observed outcomes without conflating them. A request timeout never becomes a rejection/fill assumption. Stable IDs connect execution, leg, intent, cloid, oid, fill, reservation, risk decision and PnL. Duplicates are idempotent; contradictory evidence opens reconciliation/incident state.

Restart reconstruction uses checkpoint, journal suffix and exchange reconciliation. The journal alone cannot assert current exchange truth; an exchange snapshot alone cannot explain prior decisions. Text logs are supplemental only.

P0 storage protects account, order, fill, fee, reservation, execution transition and reconciliation evidence. Required incident reconstruction also resolves the exact RunManifest, config/models/formulas, state versions and surrounding RAW market window.

Tests crash between intent/sign/send/ack/fill/cancel/recovery, truncate or duplicate journal suffixes, and inject exchange mismatch. Recovery must never blind-retry or boot READY from ambiguous evidence.
