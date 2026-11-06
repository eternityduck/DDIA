---
tags: [ddia, storage-engines]
chapter: Ch3
---

# LSM-Trees

**Definition:** Log-Structured Merge-Trees: storage engines that buffer writes in an in-memory structure (memtable), periodically flush to sorted SSTables on disk, and merge/compact them in the background.

**Why it matters:** Give very high write throughput, which is why they underlie Cassandra, RocksDB, LevelDB, and HBase.

**Example:**

```mermaid
flowchart LR
  W[write] --> MT[Memtable in RAM]
  MT -->|flush| SS1[SSTable]
  MT -->|flush| SS2[SSTable]
  SS1 & SS2 -->|compaction| SS3[Merged SSTable]
```

**Related:** [[SSTables]] [[B-Trees]] [[Compaction]] [[B-Tree vs LSM-Tree]]
