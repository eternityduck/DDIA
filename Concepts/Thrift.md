---
tags: [ddia, encoding]
chapter: Ch4
---

# Thrift

**Definition:** A binary encoding format developed at Facebook, similar in spirit to Protocol Buffers, with multiple encoding variants (BinaryProtocol, CompactProtocol).

**Why it matters:** A comparable alternative to Protocol Buffers for compact, schema-based binary encoding.

**Example:** Like Protocol Buffers, but developed at Facebook; `CompactProtocol` packs field tags and lengths into fewer bytes than Thrift's own `BinaryProtocol`.

**Related:** [[Protocol Buffers]] [[Avro]]
