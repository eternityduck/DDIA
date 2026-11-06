---
tags: [ddia, consensus]
chapter: Ch9
---

# Causality

**Definition:** An ordering that captures which events depend on which: if B happened because of A, the causal order requires A to be observed before B.

**Why it matters:** Causal consistency can be maintained without the full cost of linearizability, since it only needs to order events that are actually related.

**Example:** A reply to a comment must never be shown before the comment itself, even though they could, in principle, be stored on different replicas.

**Related:** [[Consistent Prefix Reads]] [[Total Order Broadcast]]
