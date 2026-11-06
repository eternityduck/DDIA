---
tags: [ddia, transactions]
chapter: Ch7
---

# Serializable Snapshot Isolation

**Definition:** An optimistic concurrency control technique that runs transactions on top of snapshot isolation but tracks dependencies and aborts transactions that would violate serializability.

**Why it matters:** Achieves full serializability with much better performance than two-phase locking under low contention, since it doesn't require blocking.

**Example:** Both doctors' transactions run optimistically on snapshots, but the database detects their overlapping read/write dependency and aborts one at commit time.

**Related:** [[Serializability]] [[Snapshot Isolation]]
