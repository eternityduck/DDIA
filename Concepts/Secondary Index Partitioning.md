---
tags: [ddia, partitioning]
chapter: Ch6
---

# Secondary Index Partitioning

**Definition:** Partitioning secondary indexes either by document (each partition indexes only its own documents, a local index) or by term (a global index partitioned by the indexed value).

**Why it matters:** Secondary indexes don't map neatly onto a partitioning scheme designed around the primary key, so they need their own strategy with different tradeoffs.

**Example:** An index on `color=red` either lives split across every partition (local, fast writes) or as one global partitioned-by-term index (fast reads, slower writes).

**Related:** [[Partitioning]] [[Request Routing]]
