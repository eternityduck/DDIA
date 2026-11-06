---
tags: [ddia, storage-engines]
chapter: Ch3
---

# Compaction

**Definition:** The background process of merging multiple SSTables (or log segments) into fewer, larger ones, discarding overwritten or deleted values.

**Why it matters:** Keeps the number of files bounded and reclaims disk space in log-structured storage engines.

**Example:** Three overlapping SSTables with old/overwritten values for `user:42` get merged into one SSTable that keeps only the latest value.

**Related:** [[LSM-Trees]] [[SSTables]]
