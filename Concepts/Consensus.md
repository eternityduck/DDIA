---
tags: [ddia, consensus]
chapter: Ch9
---

# Consensus

**Definition:** The problem of getting several nodes to agree on a single value or decision even if some nodes fail, formally requiring agreement, integrity, validity, and termination.

**Why it matters:** Underlies critical operations like leader election and atomic commit, which is why algorithms like Paxos and Raft exist.

**Example:** Electing a single leader among 5 nodes after the previous leader crashes, such that every surviving node agrees on who the new leader is.

**Related:** [[Paxos]] [[Raft]] [[Total Order Broadcast]]
