---
tags: [ddia, replication]
chapter: Ch5
---

# Monotonic Reads

**Definition:** A guarantee that if a user makes several reads in sequence, they will never see data go backward in time.

**Why it matters:** Prevents the confusing experience of reading replicas out of order, where time appears to move backward.

**Example:** Refreshing a comment thread and seeing a reply, then refreshing again and *not* seeing it (because you hit a more-lagging replica) is exactly what this guarantee prevents.

**Related:** [[Replication Lag]] [[Consistent Prefix Reads]]
