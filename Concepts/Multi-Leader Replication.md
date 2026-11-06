---
tags: [ddia, replication]
chapter: Ch5
---

# Multi-Leader Replication

**Definition:** Multiple nodes can each accept writes and replicate them to each other, often used across multiple datacenters.

**Why it matters:** Allows every datacenter to keep operating during a network partition between regions, at the cost of having to handle write conflicts.

**Example:**

```mermaid
flowchart LR
  L1[Leader - EU] <--> L2[Leader - US]
  C1[EU client] --> L1
  C2[US client] --> L2
```

**Related:** [[Conflict Resolution]] [[Leader-Based Replication]] [[Replication Strategies]]
