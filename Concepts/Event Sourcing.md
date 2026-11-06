---
tags: [ddia, stream-processing]
chapter: Ch11
---

# Event Sourcing

**Definition:** Storing all changes to application state as an immutable, append-only sequence of events, and deriving current state by replaying those events.

**Why it matters:** Makes application state fully auditable and lets you rebuild derived views at will, at the cost of more complex application design.

**Example:** Instead of storing `balance: 80`, store `[Deposited(100), Withdrew(20)]` — current balance is just the sum, and the full history is never lost.

**Related:** [[Change Data Capture]] [[Event Streams]]
