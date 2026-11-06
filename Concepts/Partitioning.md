---
tags: [ddia, partitioning]
chapter: Ch6
---

# Partitioning

**Definition:** Splitting a large dataset into smaller partitions (shards), each held on a different node, so different partitions can be read and written in parallel.

**Why it matters:** Necessary for scalability when a dataset or query load is too large for a single machine.

**Example:**

```mermaid
flowchart LR
  DB[(10M users)] --> P1[Partition A: users 0-3.3M]
  DB --> P2[Partition B: users 3.3M-6.6M]
  DB --> P3[Partition C: users 6.6M-10M]
```

**Related:** [[Key Range Partitioning]] [[Hash Partitioning]]
