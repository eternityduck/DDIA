---
tags: [ddia, distributed-systems]
chapter: Ch8
---

# Byzantine Faults

**Definition:** A node that doesn't just fail cleanly but behaves arbitrarily, sending corrupted, contradictory, or malicious messages to different parts of the system.

**Why it matters:** Most datacenter systems assume non-Byzantine (crash-stop) behavior and rely on operator trust rather than costly Byzantine fault tolerance.

**Example:** A node sends "write succeeded" to one peer and "write failed" to another for the same operation — most datacenter systems simply don't defend against this.

**Related:** [[Fault vs Failure]] [[Consensus]]
