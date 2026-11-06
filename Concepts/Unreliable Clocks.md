---
tags: [ddia, distributed-systems]
chapter: Ch8
---

# Unreliable Clocks

**Definition:** Machine clocks (time-of-day and monotonic clocks) that drift, jump, or get out of sync with each other due to imprecise hardware and NTP corrections.

**Why it matters:** Makes it dangerous to rely on clock readings for ordering events across machines, e.g. in determining which write happened last.

**Example:** A laptop's clock jumps backward 200ms after an NTP sync — code that assumes `now()` only ever increases can see time appear to go backward.

**Related:** [[Clock Skew]] [[Network Faults]]
