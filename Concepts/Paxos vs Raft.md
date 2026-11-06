---
tags: [ddia, consensus, comparison]
chapter: Ch9
---

# Paxos vs Raft

**Definition:** Two consensus algorithms that solve the same problem — getting a set of nodes to agree on a value despite failures — via different mechanisms: Paxos through generalized majority voting rounds, Raft through a strong elected leader and replicated log.

**Why it matters:** Raft was explicitly designed as a more implementable, understandable alternative to Paxos, which is why most newer systems pick it even though Paxos came first and is more general.

**Example:**

| | Paxos (Multi-Paxos) | Raft |
|---|---|---|
| Core idea | Two-phase majority voting per value | Elected leader replicates a log; followers just copy it |
| Leader | Implicit, emerges as an optimization | Explicit, first-class concept with terms |
| Understandability | Notoriously hard to implement correctly | Designed from the ground up to be teachable |
| Log handling | Not inherent to the base algorithm | Built-in: leader's log is the source of truth |
| Failure handling | Tolerates minority node failures | Tolerates minority node failures |
| Used by | Chubby, Spanner | etcd, Consul, CockroachDB |

**Related:** [[Paxos]] [[Raft]] [[Consensus]] [[Total Order Broadcast]]
