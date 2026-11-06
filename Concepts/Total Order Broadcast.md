---
tags: [ddia, consensus]
chapter: Ch9
---

# Total Order Broadcast

**Definition:** A protocol guaranteeing messages are delivered to all nodes reliably and in the same order.

**Why it matters:** Equivalent to solving consensus repeatedly, and the primitive used to implement state machine replication and distributed locks.

**Example:** Every node in a cluster applying the exact same sequence of config changes, in the exact same order, is equivalent to running consensus once per message.

**Related:** [[Consensus]] [[Linearizability]]
