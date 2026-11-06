---
tags: [ddia, transactions]
chapter: Ch7
---

# Two-Phase Locking

**Definition:** A concurrency control technique (distinct from two-phase commit) where transactions acquire shared or exclusive locks on objects they access and hold them until the transaction ends.

**Why it matters:** One of the oldest and most common ways to achieve true serializable isolation, at the cost of reduced concurrency and risk of deadlock.

**Example:**

```mermaid
sequenceDiagram
  participant A as Transaction A
  participant R as Row 5
  participant B as Transaction B
  A->>R: acquire write lock
  B->>R: request lock (blocks)
  A->>R: commit, release lock
  R->>B: lock granted
```
Transaction A holds a write lock on row 5 until it commits; any other transaction trying to read or write row 5 simply blocks until A finishes.

**Related:** [[Serializability]] [[Isolation Levels]]
