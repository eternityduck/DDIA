---
tags: [ddia, data-models]
chapter: Ch2
---

# Relational Model

**Definition:** Data organized into relations (tables), where each relation is an unordered collection of tuples (rows), queried via a declarative language like SQL.

**Why it matters:** Dominant model for decades due to strong support for joins, transactions, and query optimization.

**Example:**

```sql
SELECT users.name, orders.total
FROM users JOIN orders ON orders.user_id = users.id;
```

**Related:** [[Document Model]] [[Normalization]] [[Impedance Mismatch]]
