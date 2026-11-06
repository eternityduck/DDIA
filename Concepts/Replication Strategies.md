---
tags: [ddia, replication, comparison]
chapter: Ch5
---

# Replication Strategies

**Definition:** The three architectures for accepting writes across replicas: exactly one writable leader, several leaders that replicate to each other, or no leader at all with writes going to a quorum of replicas.

**Why it matters:** This choice determines whether you get write conflicts, how you handle a partitioned datacenter, and what consistency guarantees reads can offer — it's the first fork in the road for any replicated system.

**Example:**

| | Leader-Based | Multi-Leader | Leaderless |
|---|---|---|---|
| Who accepts writes | One leader | Several leaders (e.g. per region) | Any replica, via client |
| Write conflicts | Impossible (single writer) | Must be resolved (LWW, merge, custom) | Must be resolved via [[Conflict Resolution]] |
| Failover | Promote a follower | N/A — other leaders keep working | N/A — no single point of failure |
| Consistency mechanism | Replication log order | Per-leader log + conflict resolution | [[Quorum Reads and Writes]] |
| Best for | Single-region, simple topology | Multi-datacenter, offline-first apps | High write availability (Dynamo-style) |
| Examples | PostgreSQL, MySQL, MongoDB | CouchDB, multi-region mobile sync | Cassandra, DynamoDB, Riak |

**Related:** [[Leader-Based Replication]] [[Multi-Leader Replication]] [[Leaderless Replication]]
