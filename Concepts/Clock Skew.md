---
tags: [ddia, distributed-systems]
chapter: Ch8
---

# Clock Skew

**Definition:** The amount by which different machines' clocks have drifted apart from each other at a given moment.

**Why it matters:** Can silently cause data loss, e.g. in last-write-wins conflict resolution, if timestamps from skewed clocks are compared across nodes.

**Example:** Node A's clock reads 12:00:03 while Node B's reads 12:00:01 at the exact same physical moment — comparing their timestamps directly is unsafe.

**Related:** [[Unreliable Clocks]] [[Linearizability]]
