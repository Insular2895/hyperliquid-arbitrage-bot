# Checkpoint and Trace Hash Contract

`StateHash` authenticates canonical state at a cursor. DecisionTrace hash authenticates ordered trace. Prefix/suffix are cursor-bounded. Checkpoint integrity authenticates bytes/cursor. Full and checkpoint Replay require equal final state and suffix; a complete trace-hash claim additionally requires authenticated covered prefix hash/state. Missing suffix, corrupt/incompatible checkpoint or ambiguous cursor fails closed. Restart still reconciles exchange truth.
