---
tags: [ddia, distributed-systems]
chapter: Ch8
---

# Process Pauses

**Definition:** Unexpected pauses in a process's execution, such as GC pauses, VM migrations, or disk IO stalls, that can last far longer than expected.

**Why it matters:** Means a node can believe it still holds a lock or lease when everyone else has long since timed it out.

**Example:** A 30-second JVM garbage collection pause happens right after a node acquires a lock — by the time it resumes, the lock has long since expired and been given to someone else.

**Related:** [[Network Faults]] [[Fencing Tokens]]
