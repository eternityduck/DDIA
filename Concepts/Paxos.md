---
tags: [ddia, consensus]
chapter: Ch9
---

# Paxos

**Definition:** A consensus algorithm (and family of related algorithms like Multi-Paxos) that achieves agreement using two rounds of majority voting, tolerating failures of a minority of nodes.

**Why it matters:** The foundational, formally proven algorithm behind much of distributed coordination, though notoriously difficult to implement correctly.

**Example:** Multi-Paxos elects a stable leader so most writes only need one round of voting instead of two, which is how systems like Google's Chubby use it in practice.

**Related:** [[Consensus]] [[Raft]] [[Paxos vs Raft]]
