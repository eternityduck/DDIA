---
tags: [ddia, data-models]
chapter: Ch2
---

# Impedance Mismatch

**Definition:** The mismatch between the relational model's tables and an application's in-memory object or data structures, requiring a translation layer (ORM).

**Why it matters:** Document databases try to reduce this mismatch for one-to-many, tree-shaped data.

**Example:** An ORM like Hibernate exists specifically to paper over the gap between a `User` object graph and the `users`/`addresses` tables it's stored in.

**Related:** [[Relational Model]] [[Document Model]]
