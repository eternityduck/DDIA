---
tags: [ddia, consensus]
chapter: Ch9
---

# CAP Theorem

**Definition:** States that a distributed system can provide at most two of Consistency, Availability, and Partition tolerance, but since partitions will happen, the real choice during one is between consistency and availability.

**Why it matters:** Often oversimplified or misquoted; the book is critical of how much weight it's given, preferring to reason directly about linearizability vs availability tradeoffs.

**Example:**

```mermaid
flowchart TB
  CAP["Pick 2 of 3"] --- C[Consistency]
  CAP --- A[Availability]
  CAP --- P[Partition Tolerance]
  P -.during a partition, choose one.-> C
  P -.during a partition, choose one.-> A
```
During an actual network partition you can pick at most Consistency or Availability — not both.

**Related:** [[Linearizability]] [[Network Faults]]
