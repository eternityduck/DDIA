---
tags: [ddia, replication]
chapter: Ch5
---

# Consistent Prefix Reads

**Definition:** A guarantee that if a sequence of writes happens in a certain order, anyone reading those writes sees them in that same order.

**Why it matters:** Important in partitioned systems, where causally related writes could otherwise be observed out of order across partitions.

**Example:** A question and its answer, written in that causal order, must never be observed with the answer appearing before the question on some replica.

**Related:** [[Monotonic Reads]] [[Causality]]
