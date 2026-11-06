---
tags: [ddia, storage-engines, comparison]
chapter: Ch3
---

# B-Tree vs LSM-Tree

**Definition:** The two dominant families of storage engine internals, differing in whether writes update data in place (B-Tree) or are buffered and merged in sequential batches (LSM-Tree).

**Why it matters:** Picking a database often means implicitly picking one of these, and the choice determines your write throughput, read latency, and space overhead under real workloads.

**Example:**

| | B-Tree | LSM-Tree |
|---|---|---|
| Write pattern | In-place update | Sequential append (memtable → SSTable) |
| Read pattern | Few page reads, single structure | May check memtable + multiple SSTables |
| Write amplification | Lower | Higher (compaction rewrites data) |
| Read amplification | Lower | Higher without bloom filters |
| Space amplification | Lower (no stale copies) | Higher until compacted |
| Crash recovery | Write-ahead log | Log + immutable, already-durable SSTables |
| Best for | Read-heavy OLTP | Write-heavy workloads |
| Examples | PostgreSQL, MySQL (InnoDB), SQLite | Cassandra, RocksDB, LevelDB, HBase |

**Related:** [[B-Trees]] [[LSM-Trees]] [[Compaction]]
