---
tags: [ddia, replication]
chapter: Ch5
---

# Replication Lag

**Definition:** The delay between a write being applied to the leader and it becoming visible on a follower under asynchronous replication.

**Why it matters:** Under replication lag, users can observe inconsistent or stale reads, which consistency guarantees like read-your-writes try to address.

**Example:** A user posts a comment on the leader at 12:00:00; a follower a few hundred ms behind still shows the page without it at 12:00:00.3.

**Related:** [[Read-Your-Writes Consistency]] [[Monotonic Reads]]
