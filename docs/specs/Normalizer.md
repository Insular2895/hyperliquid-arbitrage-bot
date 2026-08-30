# Normalizer

## Purpose

Transformer RawEvent en contrats typés versionnés.
## Responsibilities

Parse, validate, type, dedupe hints et schema provenance.
## Non-responsibilities

Ne réordonne pas arbitrairement et ne corrige pas silencieusement le marché.
## Inputs

RawEvent, metadata/schema registry.
## Outputs

NormalizedEvent ou erreur/data-quality event.
## Dependencies

MetadataEngine, ClockAndRng.
## State

Parser/schema versions et source mapping.
## Algorithms / formulas

Conversions explicites unités/precision sans économie.
## Invariants

Payload original et lineage préservés; unknown required schema fail closed.
## Failure modes

Malformed/unknown payload, overflow, unit confusion, schema drift.
## Risk interactions

Erreur requise invalide la capability affectée.
## Performance requirements

Parsing borné, peu de copies; benchmark avant optimisation zero-copy.
## Metrics

Decode time, error/schema rates, allocation/copy diagnostics.
## Persistence

Normalized events immuables, version parser.
## Configuration

Schema/source mappings versionnés.
## Tests

Golden payloads, fuzz, boundaries, compatibility et replay parity.
## Maturity requirement

M1 avant BookEngine; M2 déterministe.
## Open calibrated parameters

Tolérance aux champs optionnels et stratégie de fallback.
