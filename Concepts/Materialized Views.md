---
tags: [ddia, storage-engines]
chapter: Ch3
---

# Materialized Views

**Definition:** A cached, precomputed copy of the result of a query, written to disk, which must be updated whenever the underlying data changes.

**Why it matters:** Speeds up read-heavy aggregate queries at the cost of write complexity and storage overhead.

**Example:** A `top_products_this_week` table that's physically recomputed and stored every hour, vs a `VIEW` that re-runs the query live on every read.

**Related:** [[Data Cubes]] [[OLTP vs OLAP]]
