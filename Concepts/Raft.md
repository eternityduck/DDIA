---
tags: [ddia, consensus]
chapter: Ch9
---

# Raft

**Definition:** A consensus algorithm designed to be more understandable than Paxos, built around strong leader election and a replicated log.

**Why it matters:** Widely adopted in real systems (etcd, Consul, CockroachDB) because its leader-based design is easier to reason about and implement.

**Example:**

```mermaid
stateDiagram-v2
  Follower --> Candidate: election timeout
  Candidate --> Leader: wins majority vote
  Leader --> Follower: discovers higher term
```

**Related:** [[Consensus]] [[Paxos]] [[Paxos vs Raft]]
