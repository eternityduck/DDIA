---
tags: [ddia, future-architecture]
chapter: Ch12
---

# Unbundling Databases

**Definition:** Viewing a database as a composition of separable components (storage engine, index, cache, replication) that can instead be assembled from separate specialized systems connected by streams of change events.

**Why it matters:** Offers a way to combine multiple specialized storage or indexing systems while keeping them consistent, as an alternative to monolithic databases.

**Example:** A Postgres table's change stream feeds both an Elasticsearch index and a Redis cache — each a specialized 'index' kept in sync outside the core database.

**Related:** [[Materialized Views]] [[Dataflow Engines]]
