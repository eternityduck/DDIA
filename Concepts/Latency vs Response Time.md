---
tags: [ddia, foundations]
chapter: Ch1
---

# Latency vs Response Time

**Definition:** Response time is what the client sees end-to-end, including queueing and network delays; latency is the duration a request spends waiting to be handled.

**Why it matters:** Conflating the two leads to measuring the wrong thing when diagnosing performance problems.

**Example:** A request with 1ms of actual processing (latency) can still have a 50ms response time once queueing delay and network round-trip are included.

**Related:** [[Percentiles]] [[Throughput]]
