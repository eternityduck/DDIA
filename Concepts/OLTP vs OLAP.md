---
tags: [ddia, storage-engines]
chapter: Ch3
---

# OLTP vs OLAP

**Definition:** OLTP (online transaction processing) serves many small reads/writes from user-facing applications; OLAP (online analytics processing) runs large aggregate queries over huge datasets for business intelligence.

**Why it matters:** The two workloads have such different access patterns that they are usually served by fundamentally different storage engines.

**Example:** OLTP: "update this one customer's address" (touches 1 row). OLAP: "total revenue by region for 2025" (scans millions of rows, touches 2 columns).

**Related:** [[Column-Oriented Storage]] [[Data Cubes]]
