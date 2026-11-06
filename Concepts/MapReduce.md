---
tags: [ddia, batch-processing]
chapter: Ch10
---

# MapReduce

**Definition:** A batch processing framework that runs a map function over input records (emitting key-value pairs) and a reduce function that aggregates values sharing a key, with sorting and shuffling in between.

**Why it matters:** Popularized distributed batch processing on commodity hardware (Hadoop), though largely superseded in practice by more flexible dataflow engines.

**Example:**

```mermaid
flowchart LR
  Input --> Map1[map] --> Shuffle
  Input --> Map2[map] --> Shuffle
  Shuffle --> Reduce1[reduce] --> Output
  Shuffle --> Reduce2[reduce] --> Output
```

**Related:** [[Distributed Filesystems]] [[Join Algorithms]]
