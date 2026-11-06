---
tags: [ddia, foundations]
chapter: Ch1
---

# Percentiles

**Definition:** Response time is best summarized as percentiles (p50 median, p95, p99, p999) rather than an average, since averages hide the tail latency that affects real users.

**Why it matters:** High percentiles ('tail latencies') directly affect the users with the slowest requests, often the most valuable ones.

**Example:** p50 = 50ms, p95 = 200ms, p999 = 2s — the p999 user is often your biggest customer, with the most data to load.

**Related:** [[Latency vs Response Time]] [[Scalability]]
