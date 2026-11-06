---
tags: [ddia, encoding]
chapter: Ch4
---

# Schema Evolution

**Definition:** The process of changing a data schema over time (adding, removing, or renaming fields) while old and new code and data continue to coexist.

**Why it matters:** Schemas inevitably change over time, so systems need a graceful way to handle it without downtime.

**Example:** Adding an optional `middle_name` field with a default value of `null` so both old and new application code keep working.

**Related:** [[Backward and Forward Compatibility]] [[Avro]]
