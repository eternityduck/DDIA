---
tags: [ddia, storage-engines]
chapter: Ch3
---

# Bloom Filter

**Definition:** A memory-efficient probabilistic data structure that can tell you a key is 'definitely not present' or 'possibly present,' with no false negatives.

**Why it matters:** Lets LSM-tree storage engines avoid expensive disk lookups across SSTables for keys that don't exist.

**Example:** Checking for key `"xyz"` across 10 SSTables: the bloom filter says 'definitely not in files 1-9, maybe in file 10' — saving 9 unnecessary disk reads.

**Related:** [[SSTables]] [[LSM-Trees]]
