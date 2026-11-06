---
tags: [ddia, foundations]
chapter: Ch1
---

# Fault vs Failure

**Definition:** A fault is one component deviating from its spec; a failure is when the system as a whole stops providing the required service to the user.

**Why it matters:** Fault-tolerant systems are built to prevent faults from cascading into failures, e.g. via redundancy.

**Example:** A single disk dying in a RAID array is a fault; the database going down because of it is a failure — redundancy is what keeps one from becoming the other.

**Related:** [[Reliability]] [[Byzantine Faults]]
