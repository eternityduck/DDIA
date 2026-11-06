---
tags: [ddia, encoding]
chapter: Ch4
---

# Avro

**Definition:** A binary encoding format (from the Hadoop project) that encodes data with no field tags, relying on a separately stored schema for both writer and reader to interpret the data.

**Why it matters:** Well suited to large files and dynamically generated schemas, since writer and reader schemas can differ without explicit field numbering.

**Example:** The writer encodes `{"name": "Bill"}` as raw bytes with no field tags at all — the reader only knows what the bytes mean because it has a copy of the writer's schema.

**Related:** [[Protocol Buffers]] [[Schema Evolution]]
