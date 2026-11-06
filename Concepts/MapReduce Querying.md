---
tags: [ddia, data-models, batch-processing]
chapter: Ch2
---

# MapReduce Querying

**Definition:** A programming model for processing large amounts of data across many machines by alternating a map function (over each record) and a reduce function (aggregating results), used by some databases as a querying mechanism between fully declarative and fully imperative.

**Why it matters:** Bridges distributed batch processing with database querying for large-scale aggregation jobs.

**Example:** MongoDB's old `mapReduce` command let you write a `map` function emitting `(category, 1)` per document and a `reduce` function summing them — a middle ground between full SQL and hand-written application code.

**Related:** [[Declarative vs Imperative Query Languages]] [[MapReduce]]
