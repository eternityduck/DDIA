---
tags: [ddia, distributed-systems]
chapter: Ch8
---

# Network Faults

**Definition:** Packets being lost, delayed, or reordered on an unreliable network, with no reliable way to tell the difference between a slow node and a dead one.

**Why it matters:** Forces distributed systems to use timeouts as an imperfect heuristic and to design for a 'failed' node that might actually still be running.

**Example:** A request times out after 5 seconds — but there's no way to know if the server crashed, the response was lost, or it's just slow and about to arrive.

**Related:** [[Unreliable Clocks]] [[Process Pauses]]
