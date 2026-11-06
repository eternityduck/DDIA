---
tags: [ddia, foundations]
chapter: Ch1
---

# Scalability

**Definition:** A system's ability to cope with increased load (more data, more traffic, more complexity), described using load parameters such as requests/sec, read/write ratio, or number of active users.

**Why it matters:** Determines when and how you need to add resources (scale up vs scale out) as a product grows.

**Example:** Twitter's early 'fail whale' outages: celebrity accounts made the read-heavy timeline load pattern (fan-out on read) buckle, pushing them toward fan-out on write.

**Related:** [[Load Parameters]] [[Throughput]] [[Percentiles]]
