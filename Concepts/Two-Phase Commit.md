---
tags: [ddia, consensus]
chapter: Ch9
---

# Two-Phase Commit

**Definition:** An atomic commit protocol where a coordinator first asks all participants to prepare (promise they can commit), and only tells them to actually commit if all agree.

**Why it matters:** The standard way to achieve atomicity across multiple nodes or databases, but it blocks if the coordinator fails mid-protocol.

**Example:**

```mermaid
sequenceDiagram
  Coordinator->>DB1: prepare
  Coordinator->>DB2: prepare
  DB1-->>Coordinator: yes
  DB2-->>Coordinator: yes
  Coordinator->>DB1: commit
  Coordinator->>DB2: commit
```

**Related:** [[Atomicity]] [[Consensus]]
