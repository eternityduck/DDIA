---
tags: [ddia, storage-engines]
chapter: Ch3
---

# Column-Oriented Storage

**Definition:** Storing all values from each column together on disk rather than storing each row contiguously.

**Why it matters:** Dramatically speeds up analytic queries that scan a few columns across many rows, and compresses extremely well.

**Example:** Row storage: `[id,name,price],[id,name,price],...` on disk. Column storage: all `id`s together, then all `name`s, then all `price`s — so `AVG(price)` reads only the price column.

**Related:** [[OLTP vs OLAP]] [[Data Cubes]]
