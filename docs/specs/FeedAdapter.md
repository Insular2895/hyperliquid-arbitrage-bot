# FeedAdapter

## Purpose

Convertir une source live/replay en flux brut ordonné et observable.
## Responsibilities

Connexion, bootstrap, reconnect, source timestamps/sequences et health.
## Non-responsibilities

Ne construit pas le book et ne décide jamais un trade.
## Inputs

Endpoint/config/source credentials ou ReplayFeed.
## Outputs

RawEvent et FeedHealth typés.
## Dependencies

ClockAndRng, Recorder; règles exchange revalidées.
## State

ConnectionId, last event/sequence, reconnect/backoff et capability.
## Algorithms / formulas

Ordonnancement source; aucune formule économique.
## Invariants

Chaque payload reçu est attribuable; gap/reconnect jamais caché.
## Failure modes

Disconnect, duplicate, reorder, gap, malformed payload, stale stream.
## Risk interactions

Invalidité/gap retire readiness des marchés affectés.
## Performance requirements

Travail borné; aucune I/O annexe bloquant la réception.
## Metrics

Messages/drops/gaps, recv latency, age, reconnects, decode handoff.
## Persistence

RawEvent via Recorder; connection lifecycle.
## Configuration

Endpoints, subscriptions, backoff, source priority versionnés.
## Tests

Fixtures, malformed/reorder/duplicate/gap/reconnect et load.
## Maturity requirement

M1 fixtures; M2 replay; M3 live shadow avant ordre.
## Open calibrated parameters

Backoff, staleness et préférence de feed.
