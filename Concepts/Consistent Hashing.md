---
tags: [ddia, partitioning]
chapter: Ch6
---

# Consistent Hashing

**Definition:** A hashing scheme where adding or removing a node only requires moving a small, bounded fraction of keys instead of reshuffling almost everything.

**Why it matters:** Minimizes data movement during rebalancing, which is critical as a cluster grows or shrinks.

**Example:**

```mermaid
flowchart LR
  subgraph Ring["Hash ring (clockwise)"]
    A((Node A)) --> B((Node B))
    B --> D((New Node D))
    D --> C((Node C))
    C --> A
  end
```
Only the keys between D's position and the next node clockwise move to D — every other node's keys stay put.

**Related:** [[Hash Partitioning]] [[Rebalancing Partitions]]
