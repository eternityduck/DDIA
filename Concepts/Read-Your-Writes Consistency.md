---
tags: [ddia, replication]
chapter: Ch5
---

# Read-Your-Writes Consistency

**Definition:** A guarantee that if a user submits a write, they will always see it reflected on a subsequent read, even if that read goes to a lagging replica.

**Why it matters:** Without it, users would see their own submitted data disappear, which feels broken.

**Example:** You update your profile photo, then immediately reload the page — without this guarantee, a lagging replica could serve you the old photo back.

**Related:** [[Replication Lag]] [[Monotonic Reads]]
