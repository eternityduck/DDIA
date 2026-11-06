---
tags: [ddia, partitioning]
chapter: Ch6
---

# Hash Partitioning

**Definition:** Assigning partitions based on a hash of the key, spreading keys pseudo-randomly across partitions.

**Why it matters:** Distributes load evenly and avoids hot spots, but sacrifices the ability to do efficient range queries.

**Example:**

```mermaid
flowchart LR
  K1[user_id: 17] -->|hash % 3 = 0| N0[Node 0]
  K2[user_id: 42] -->|hash % 3 = 1| N1[Node 1]
  K3[user_id: 99] -->|hash % 3 = 2| N2[Node 2]
```
`hash(user_id) % 3` sends roughly equal traffic to each of 3 nodes, but makes "find all users between IDs 100-200" impossible to answer from one partition.

**Related:** [[Partitioning]] [[Consistent Hashing]]
