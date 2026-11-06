---
tags: [ddia, partitioning]
chapter: Ch6
---

# Key Range Partitioning

**Definition:** Assigning each partition a continuous range of keys (like the volumes of an encyclopedia), keeping keys sorted within a partition.

**Why it matters:** Makes range queries efficient, but risks hot spots if certain key ranges (e.g. today's timestamp) are written far more than others.

**Example:**

```mermaid
flowchart LR
  Node1["Node 1: A-H"] --- Node2["Node 2: I-P"] --- Node3["Node 3: Q-Z"]
```
`[A-H] -> Node1, [I-P] -> Node2, [Q-Z] -> Node3` — but if everyone's key starts with today's date, one partition gets all the traffic.

**Related:** [[Partitioning]] [[Rebalancing Partitions]]
