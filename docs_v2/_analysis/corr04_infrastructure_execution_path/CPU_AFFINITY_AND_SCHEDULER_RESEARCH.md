# CPU Affinity and Scheduler Research

`STATUS: EVIDENCE-GATED HOST OPTIMIZATION`

Linux affinity constrains eligible CPUs and can reduce migrations/cache disruption, but cpusets/permissions and the scheduler still apply. Real-time policies can starve normal work and a runaway task can impair the host. Sources: [`sched_setaffinity(2)`](https://man7.org/linux/man-pages/man2/sched_setaffinity.2.html), [`sched(7)`](https://man7.org/linux/man-pages/man7/sched.7.html), [kernel RT group scheduling](https://docs.kernel.org/scheduler/sched-rt-group.html).

First attribute queue wait: scheduler delay, run queue, migrations, context switches, steal, IRQ load, CPU frequency/throttling, page faults and co-located node/Recorder work. Pinning is a treatment only when those measurements implicate scheduling.

Compare unpinned baseline, hot-thread affinity, support-thread separation and, only where justified, priority/nice candidates. A 2-vCPU VPS may worsen when pinning crowds feed, account/fill/reconciliation and Recorder work; no hot thread may starve those safety paths. `SCHED_FIFO`/RT is never applied blindly. Steal time is generally outside guest control and may favor a dedicated-host experiment instead.

Promotion requires identical correctness, no safety starvation, stable tail gain across regimes, explicit CPU mask/topology/SMT/NUMA context, rollback and capture/economic relevance.
