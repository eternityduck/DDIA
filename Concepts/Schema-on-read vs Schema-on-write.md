---
tags: [ddia, data-models]
chapter: Ch2
---

# Schema-on-read vs Schema-on-write

**Definition:** Schema-on-write (relational) enforces structure before data is stored; schema-on-read (document databases) interprets structure only when data is read, so different records can have different shapes.

**Why it matters:** Schema-on-read gives more flexibility for evolving applications, similar to dynamic typing in programming languages.

**Example:** Adding a new optional field to a MongoDB document (schema-on-read) requires no migration; adding a column to a Postgres table (schema-on-write) does.

**Related:** [[Document Model]] [[Schema Evolution]]
