---
tags: [ddia, storage-engines]
chapter: Ch3
---

# SSTables

**Definition:** Sorted String Tables: an on-disk file format storing key-value pairs sorted by key, enabling efficient merging, range queries, and sparse in-memory indexes.

**Why it matters:** The core persisted file format underlying LSM-tree storage engines like LevelDB and Cassandra.

**Example:**

```mermaid
flowchart TB
  Idx["Sparse index: apple, cherry, lime, ..."] --> File["SSTable file (sorted): apple, apricot, ..., cherry, ..., lime, ..., zebra"]
```
A 100MB SSTable file holding keys `"apple"..."zebra"` sorted alphabetically, with a sparse index pointing to every 64th key for fast lookups.

**Related:** [[LSM-Trees]] [[Log-Structured Storage]]
