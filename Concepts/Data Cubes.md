---
tags: [ddia, storage-engines]
chapter: Ch3
---

# Data Cubes

**Definition:** A grid of aggregated values (e.g. sums) across two or more dimensions, letting you quickly look up pre-computed aggregates without scanning raw data.

**Why it matters:** A special case of a materialized view useful for OLAP workloads with regularly sliced-and-diced queries, but inflexible for ad hoc ones.

**Example:** A 2D cube of `revenue` by `(date, product_category)` lets you look up "furniture sales on 2026-10-15" instantly without scanning raw orders.

**Related:** [[Materialized Views]] [[OLTP vs OLAP]]
