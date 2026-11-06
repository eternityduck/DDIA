---
tags: [ddia, partitioning]
chapter: Ch6
---

# Rebalancing Partitions

**Definition:** The process of moving data and request load from one node to another as nodes are added or removed from a cluster.

**Why it matters:** Needs to happen with minimal disruption and minimal unnecessary data movement.

**Example:** Adding a 4th node to a 3-node cluster should move roughly 1/4 of the data, not trigger a full reshuffle of everything.

**Related:** [[Partitioning]] [[Consistent Hashing]]
