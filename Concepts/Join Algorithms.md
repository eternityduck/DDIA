---
tags: [ddia, batch-processing]
chapter: Ch10
---

# Join Algorithms

**Definition:** Techniques for joining datasets in a batch context without an index: sort-merge joins (both inputs sorted by join key then merged) and broadcast hash joins (small input held in memory on every node).

**Why it matters:** Making the join algorithm explicit, rather than relying on an optimizer, is a key difference between batch dataflow and traditional databases.

**Example:** Sort-merge join: sort both `orders` and `users` by `user_id`, then walk both sorted lists together like a zipper, matching rows in one linear pass.

**Related:** [[MapReduce]] [[Dataflow Engines]]
