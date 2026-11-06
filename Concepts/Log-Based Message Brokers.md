---
tags: [ddia, stream-processing]
chapter: Ch11
---

# Log-Based Message Brokers

**Definition:** Brokers (e.g. Apache Kafka) that durably append messages to a partitioned log, letting multiple consumers independently track their own read position and replay old messages.

**Why it matters:** Combines the durability of a database log with the pub/sub pattern of a message broker, central to building scalable stream-processing pipelines.

**Example:**

```mermaid
flowchart LR
  P[Producer] --> Log[(Partitioned log)]
  Log --> CG1[Consumer group A @offset 102]
  Log --> CG2[Consumer group B @offset 97]
```

**Related:** [[Message Brokers]] [[Change Data Capture]]
