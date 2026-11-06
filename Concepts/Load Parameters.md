---
tags: [ddia, foundations]
chapter: Ch1
---

# Load Parameters

**Definition:** Numbers that describe the load on a system, e.g. requests per second, ratio of reads to writes, number of simultaneously active users, or cache hit rate, chosen based on the specific architecture.

**Why it matters:** You need the right load parameters before you can reason about scalability for your particular system.

**Example:** Twitter's two timeline designs (query-time join vs fan-out-on-write) are each optimized for a different load parameter: read-heavy vs write-heavy.

**Related:** [[Scalability]] [[Throughput]]
