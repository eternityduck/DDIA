---
tags: [ddia, transactions]
chapter: Ch7
---

# Snapshot Isolation

**Definition:** Each transaction reads from a consistent snapshot of the database as of when it started, typically implemented via multi-version concurrency control (MVCC).

**Why it matters:** Solves read skew (non-repeatable reads), which matters for backups and long-running analytic queries.

**Example:** A nightly backup job reads a consistent view of the whole database as it was at 2am, even though writes keep happening at 2:01, 2:02, etc.

**Related:** [[Isolation Levels]] [[Write Skew]] [[Isolation Level Ladder]]
