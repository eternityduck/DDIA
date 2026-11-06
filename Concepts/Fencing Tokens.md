---
tags: [ddia, consensus]
chapter: Ch9
---

# Fencing Tokens

**Definition:** A monotonically increasing token issued by a lock or lease service each time a lock is granted, which downstream systems can use to reject writes from a client holding a stale lock.

**Why it matters:** Protects against the dangerous case where a paused process wakes up believing it still holds a lock it has actually lost.

**Example:** Lock granted with token 33, client pauses, lock expires and is re-granted with token 34 to another client — storage rejects any write tagged with token 33 after that.

**Related:** [[Process Pauses]] [[Leader-Based Replication]]
