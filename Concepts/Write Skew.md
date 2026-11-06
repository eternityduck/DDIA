---
tags: [ddia, transactions]
chapter: Ch7
---

# Write Skew

**Definition:** A race condition where two transactions read the same data, then each makes a different write based on what they read, and the combination violates an invariant that held when each transaction checked it.

**Why it matters:** Not prevented by snapshot isolation, and easy to miss because it doesn't look like a classic write-write conflict.

**Example:** Two on-call doctors both check "is at least one other doctor on call?", both see yes, and both go off-call — leaving zero doctors on call despite the invariant.

**Related:** [[Snapshot Isolation]] [[Phantom Reads]]
