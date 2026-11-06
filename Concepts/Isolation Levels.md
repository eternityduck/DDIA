---
tags: [ddia, transactions]
chapter: Ch7
---

# Isolation Levels

**Definition:** Weaker-than-full-serializability guarantees (such as read committed or snapshot isolation) that databases offer by default, trading some anomalies for better performance.

**Why it matters:** True serializability is often too slow, so most databases default to a weaker level, and you need to understand which anomalies that permits.

**Example:** Read committed stops you seeing uncommitted writes; snapshot isolation stops your long report query from seeing *any* writes made after it started.

**Related:** [[Read Committed]] [[Snapshot Isolation]] [[Serializability]] [[Isolation Level Ladder]]
