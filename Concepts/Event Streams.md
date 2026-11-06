---
tags: [ddia, stream-processing]
chapter: Ch11
---

# Event Streams

**Definition:** A continuous flow of events, small immutable facts about something that happened, that producers emit and consumers process, often over a log-based broker.

**Why it matters:** The core abstraction stream processing is built on, letting you treat unbounded, continuously arriving data uniformly.

**Example:** `UserSignedUp`, `OrderPlaced`, `PaymentFailed` — each a small immutable fact, flowing continuously rather than sitting in one queryable table.

**Related:** [[Message Brokers]] [[Event Sourcing]]
