---
tags: [ddia, transactions]
chapter: Ch7
---

# Phantom Reads

**Definition:** A write in one transaction changes the result of a search query that a concurrent transaction already ran, as if a new row had 'phantom' appeared.

**Why it matters:** A particularly subtle cause of write skew, since the affected rows didn't even exist when the first transaction read.

**Example:** A query counting "doctors on call" returns 2, satisfying a check — but a concurrent transaction inserts a new doctor row, retroactively invalidating that count.

**Related:** [[Write Skew]] [[Serializability]]
