# IRQ and Network Queue Research

`STATUS: RESEARCH — AVAILABILITY HOST-DEPENDENT`

Linux RSS maps flows to hardware receive queues/IRQs; RPS performs software receive steering; RFS extends it toward the consuming application CPU. IRQ affinity controls eligible CPUs, while `irqbalance`, virtual NICs and provider policy may override or hide control. Sources: [Linux scaling](https://docs.kernel.org/networking/scaling.html), [IRQ affinity](https://docs.kernel.org/core-api/irq/irq-affinity.html).

Before treatment, record NIC/driver/queue count, interrupt distribution, softirq load, drops, CPU topology, application CPU and whether the VPS exposes controllable IRQs. Compare RSS alone, RPS/RFS where relevant and explicit IRQ/queue placement only after a measured bottleneck.

Same-core NIC/application placement can improve locality or harm latency through interrupt/softirq contention. More queues or cross-core steering can add reordering, IPIs and cache traffic. Correctness, connection stability, loss, scheduler tails and account/reconciliation progress are guardrails. If the guest lacks control, record `NOT_APPLICABLE`; do not simulate evidence.
