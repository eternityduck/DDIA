---
tags: [ddia, partitioning]
chapter: Ch6
---

# Request Routing

**Definition:** The problem of a client or load balancer determining which node to connect to for a given partitioned key, solved via a routing tier, gossip protocol, or a coordination service like ZooKeeper.

**Why it matters:** In a partitioned system, clients need a way to discover the current partition-to-node mapping, especially as rebalancing happens.

**Example:** A client asks ZooKeeper "which node owns partition 7 right now?" before sending its read — and gets notified if that mapping changes mid-session.

**Related:** [[Partitioning]] [[Secondary Index Partitioning]]
