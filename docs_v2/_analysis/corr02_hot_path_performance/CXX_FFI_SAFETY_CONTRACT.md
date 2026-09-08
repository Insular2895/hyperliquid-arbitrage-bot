# C++ FFI Safety Contract

DOCUMENTATION STATUS: CONDITIONAL FUTURE CONTRACT — NO FFI AUTHORIZED

If the escalation gate ever passes, the boundary must satisfy:

- narrow `extern "C"` ABI with fixed-width scalars, explicit discriminants and `repr(C)`-compatible POD/header+buffer views;
- no Rust `Vec`, `String`, trait object, reference graph, callback ownership or language-native exception type in the ABI;
- every buffer carries pointer/nullability, length, capacity/ownership where relevant and lifetime rules;
- allocation/free occur on the same side, or use an explicit paired allocator API with layout/version tests;
- no C++ exception or Rust panic crosses the boundary; functions return explicit status/error and validate all inputs;
- no retained pointer to temporary Rust memory and no mutation outside declared output buffers;
- thread affinity/concurrency/reentrancy are explicit; foreign code does not acquire domain ownership;
- ABI version, struct size/alignment/endian/numeric representation and library/build identity are checked;
- faults are tested with fuzzing, sanitizers, malformed inputs, OOM/boundaries, Replay and process-crash recovery;
- FFI call, marshalling, copying and cache effects are included in the benchmark.

Rust remains the semantic oracle. Exact output/reason/version equality is required; a faster discrepant result fails. A crash cannot be treated as a recoverable ordinary error unless process architecture and reconciliation prove that property in a later approved design.
