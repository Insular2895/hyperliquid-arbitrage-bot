# RNG Seed Determinism Contract

No active decision RNG permits absent `random_seed`. Active Monte Carlo, probabilistic fill/queue/participant or randomized policy requires a versioned seed; absence invalidates a deterministic claim. Deterministic floating inference is not RNG. Same seed/inputs must match; a different seed is a distinct run. Stream partitioning is an OPEN implementation design, but scheduling independence is mandatory.
