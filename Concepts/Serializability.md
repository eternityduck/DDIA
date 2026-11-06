---
tags: [ddia, transactions]
chapter: Ch7
---

# Serializability

**Definition:** The strongest isolation level, guaranteeing the result of concurrently executing transactions is the same as if they had run one at a time, in some order.

**Why it matters:** Eliminates every possible race condition, but often at a real performance cost, which is why systems offer weaker levels by default.

**Example:** If two transactions each read the account balance then independently add $10, true serializability guarantees the result is $20 total added, not $10 silently lost.

**Related:** [[Two-Phase Locking]] [[Serializable Snapshot Isolation]] [[Isolation Level Ladder]]
