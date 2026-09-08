# CORR-02 — External Performance Research

DOCUMENTATION STATUS: COMPARATIVE / IMPLEMENTATION RESEARCH — NOT A CANONICAL SOURCE

Research was revalidated on 2026-09-08. These sources constrain future experiments; they do not add `SRC-009`, select an implementation or authorize a runtime change.

## Harjus comparison

| Field | Value |
|---|---|
| Repository | [ValtteriL/harjus](https://github.com/ValtteriL/harjus) |
| Inspected commit | `09816b3da2a393795250e38c8b49869b57ba4d6f` |
| Commit time | 2026-03-04T20:34:31+02:00 |
| Classification | `COMPARATIVE_EXTERNAL_EVIDENCE` |

At that commit, Harjus precomputes triangular paths, uses an `unordered_multimap<string, index>` to select affected opportunities, carries BBO price/quantity updates through bounded Boost SPSC queues and evaluates a single worker-owned opportunity set. It also copies some vectors/strings in the evaluated path. These observations motivate measuring work amplification, indexing, copies and queueing. They do not prove that the same structures, C++, kernel bypass, FIX/FOK or Binance-specific economics fit Hyperliquid.

## Rust compiler and containers

| Primary source | Verified fact | CORR-02 consequence |
|---|---|---|
| [Cargo profiles](https://doc.rust-lang.org/cargo/reference/profiles.html) | `release` is optimized, but LTO is off and non-incremental codegen defaults to multiple codegen units; LTO/codegen units trade build time against possible runtime performance. | Compare controlled build variants; do not declare a flag universally faster. |
| [rustc codegen options](https://doc.rust-lang.org/rustc/codegen-options/index.html#target-cpu) | `target-cpu=native` targets the build host; target features affect compatibility and unsafe feature use can produce invalid runtime behavior. | A native build is not automatically portable to every client OCI host; artifact targeting is a later deployment decision. |
| [rustc PGO](https://doc.rust-lang.org/rustc/profile-guided-optimization.html) | PGO uses an instrumented training build and a separate profile-use build. | Training must represent production workloads; the instrumented binary is not the production comparator. |
| [`Vec` guarantees](https://doc.rust-lang.org/std/vec/struct.Vec.html#guarantees) | Elements are contiguous; capacity is reliable for `push`/`insert`; clearing and refilling within capacity avoids allocator calls; growth strategy and ABI field order are not guaranteed. | Preallocation/reuse is a valid candidate, but capacity source, growth fallback and ABI boundaries must be explicit. |
| [Atomic ordering](https://doc.rust-lang.org/std/sync/atomic/enum.Ordering.html) | Acquire/Release establish specific causality; `Relaxed` provides atomicity without a happens-before relation; `SeqCst` adds a global order. | Every atomic gets a written memory-order invariant; neither blanket `Relaxed` nor blanket `SeqCst` is acceptable. |

`panic=abort`, Thin/Fat LTO, one/fewer codegen units, `target-cpu`, PGO, BOLT-like post-link layout and SIMD remain benchmark candidates only. Debuggability, crash behavior, build reproducibility, client portability and representative training are part of the comparison.

## Linux/perf evidence

| Primary source | Verified fact | Use |
|---|---|---|
| [`perf stat`](https://man7.org/linux/man-pages/man1/perf-stat.1.html) | Can count task clock, context switches, migrations, page faults, cycles, instructions, branches and branch misses. | Attribute CPU, scheduler and fault effects; retain raw counts and supported-event metadata. |
| [`perf_event_open`](https://man7.org/linux/man-pages/man2/perf_event_open.2.html) | Cache events are CPU-specific; cycles can be affected by frequency scaling; reference cycles and page-fault classes differ. | Never compare unnamed counters across different hosts/PMUs as if identical. |
| [`perf sched`](https://man7.org/linux/man-pages/man1/perf-sched.1.html) | Reports runtime, scheduling delay and wake/migration history. | Separate runnable delay/queueing from component execution time. |
| [`perf list`](https://man7.org/linux/man-pages/man1/perf-list.1.html) | Counter multiplexing may introduce error; grouped events reduce mismatch but are limited by available PMU counters. | Record enabled/running ratios and avoid overloading one run with every counter. |
| [Kernel allocation profiling](https://docs.kernel.org/mm/allocation-profiling.html) | Kernel allocation profiling is configurable and has its own overhead/availability conditions. | Treat allocation instrumentation as a special measurement mode, not silent always-on production truth. |

Application-heap allocation counts require a suitable user-space mechanism selected later. Kernel `/proc/allocinfo` does not substitute for Rust heap-allocation attribution.

## FFI safety

| Primary source | Verified fact | Required boundary |
|---|---|---|
| [Rust Nomicon FFI](https://doc.rust-lang.org/nomicon/ffi.html) | Foreign calls are unsafe; unwinding behavior depends on ABI; a foreign exception entering a non-unwind Rust boundary can be undefined behavior. | No exception or panic crosses the boundary; explicit status/error output and crash tests are mandatory. |
| [`repr(C)`](https://doc.rust-lang.org/nomicon/other-reprs.html#reprc) | `repr(C)` establishes C-compatible layout for suitable types, while some Rust types remain unsuitable. | Use fixed-width C-compatible POD/header+buffer views; never expose Rust-native layout implicitly. |
| [`Vec` guarantees](https://doc.rust-lang.org/std/vec/struct.Vec.html#guarantees) | `Vec` storage is contiguous but its ABI layout is not stable, and allocator/layout ownership matters for reconstruction/deallocation. | No Rust `Vec`/`String` ABI. Allocation and deallocation remain on the same side or use an explicit ownership API. |

No FFI library, binding generator, C++ standard library, allocator or candidate kernel is selected. Rust remains the oracle and production baseline.
