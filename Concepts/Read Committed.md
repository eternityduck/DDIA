---
tags: [ddia, transactions]
chapter: Ch7
---

# Read Committed

**Definition:** The default isolation level in many databases, guaranteeing you only ever read committed data (no dirty reads) and only overwrite committed data (no dirty writes).

**Why it matters:** Prevents the most obviously confusing races, but still allows race conditions like read skew and lost updates.

**Example:** Transaction A is halfway through updating 10 rows; Transaction B running `SELECT` concurrently sees either all-old or all-new values per row, never an uncommitted partial value.

**Related:** [[Isolation Levels]] [[Snapshot Isolation]] [[Isolation Level Ladder]]
