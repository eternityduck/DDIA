---
tags: [ddia, replication]
chapter: Ch5
---

# Conflict Resolution

**Definition:** Techniques such as last-write-wins, version vectors, CRDTs, or application-level merge logic for reconciling concurrently written values.

**Why it matters:** Any system allowing concurrent writes to the same data (multi-leader or leaderless) must decide how to resolve conflicting versions.

**Example:** Two offline clients both set a shopping cart's quantity field concurrently; last-write-wins picks one by timestamp, while a CRDT could instead merge both intents.

**Related:** [[Multi-Leader Replication]] [[Leaderless Replication]]
