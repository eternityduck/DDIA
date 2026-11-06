---
tags: [ddia, batch-processing]
chapter: Ch10
---

# Distributed Filesystems

**Definition:** A filesystem (like HDFS) that stores files across many machines, replicating blocks for fault tolerance and co-locating compute with the data it stores.

**Why it matters:** Provides the durable, scalable storage layer that batch processing frameworks like MapReduce run on top of.

**Example:** A 1GB file is split into 128MB blocks, each replicated 3x across different machines in HDFS — so a single disk failure never loses data.

**Related:** [[MapReduce]] [[Dataflow Engines]]
