---
tags: [ddia, stream-processing]
chapter: Ch11
---

# Exactly-Once Semantics

**Definition:** A guarantee that a message or event is processed effectively once, even though the underlying network and brokers can only guarantee at-least-once or at-most-once delivery.

**Why it matters:** Usually achieved through idempotent operations or transactional/fencing techniques, since true exactly-once delivery is impossible in general.

**Example:** A payment consumer uses the order ID as an idempotency key, so even if Kafka redelivers the same message twice, the charge only happens once.

**Related:** [[Message Brokers]] [[Fencing Tokens]]
