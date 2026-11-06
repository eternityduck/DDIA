---
tags: [ddia, encoding]
chapter: Ch4
---

# Protocol Buffers

**Definition:** A binary encoding format from Google using numbered fields and a compact tagged encoding, requiring a schema to encode and decode.

**Why it matters:** Compact and fast compared to JSON/XML, with built-in schema evolution rules for compatibility.

**Example:**

```protobuf
message Person {
  required string name = 1;
  optional int32 age = 2;
}
```
Field numbers (`1`, `2`), not names, are what's actually encoded on the wire.

**Related:** [[Thrift]] [[Avro]]
