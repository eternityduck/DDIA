---
tags: [ddia, data-models]
chapter: Ch2
---

# Document Model

**Definition:** Data stored as self-contained documents (e.g. JSON), with better locality for one-to-many tree structures but weaker support for many-to-many relationships.

**Why it matters:** Reduces impedance mismatch for application code that already works with nested object structures.

**Example:**

```json
{
  "name": "Bill",
  "jobs": ["writer", "farmer"]
}
```
The whole resume lives in one self-contained document instead of being spread across joined tables.

**Related:** [[Relational Model]] [[Schema-on-read vs Schema-on-write]]
