---
tags: [ddia, transactions]
chapter: Ch7
---

# ACID

**Definition:** Atomicity, Consistency, Isolation, Durability: the classical safety guarantees offered by transactions.

**Why it matters:** A widely used shorthand for transaction safety, though the book argues 'consistency' doesn't really belong alongside the other three, which are genuinely about the database's own guarantees.

**Example:** A bank transfer debits account A and credits account B inside one transaction — atomicity guarantees you never see a state where A lost money but B didn't gain it.

**Related:** [[Atomicity]] [[Isolation Levels]]
