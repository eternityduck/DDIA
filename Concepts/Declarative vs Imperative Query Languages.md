---
tags: [ddia, data-models]
chapter: Ch2
---

# Declarative vs Imperative Query Languages

**Definition:** Declarative languages (SQL) state what result is wanted and let the database decide how to get it; imperative code specifies the exact steps to take.

**Why it matters:** Declarative queries give the query optimizer freedom to improve performance without changing application code.

**Example:** `SELECT * FROM users WHERE age > 30` (declarative) vs manually looping over a list and checking `if user.age > 30` (imperative) — the database picks the execution plan for the former.

**Related:** [[MapReduce Querying]]
