---
tags: [ddia, transactions, comparison]
chapter: Ch7
---

# Isolation Level Ladder

**Definition:** The progression of transaction isolation guarantees from weakest to strongest, where each rung prevents more anomalies at the cost of more coordination overhead.

**Why it matters:** Most databases default to something weaker than serializable, so you need to know exactly which race conditions your chosen level still permits — the book's running theme is that these names are commonly misunderstood.

**Example:**

| Level | Dirty reads | Read skew | Lost updates | Write skew / phantoms |
|---|---|---|---|---|
| Read Committed | Prevented | Possible | Possible | Possible |
| Snapshot Isolation | Prevented | Prevented | Prevented (via detection) | Possible |
| Serializable | Prevented | Prevented | Prevented | Prevented |

Going up the ladder trades concurrency/performance for fewer anomalies; [[Two-Phase Locking]] and [[Serializable Snapshot Isolation]] are the two main ways to reach the top rung.

**Related:** [[Read Committed]] [[Snapshot Isolation]] [[Serializability]] [[Write Skew]]
