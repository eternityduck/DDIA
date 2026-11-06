---
tags: [ddia, batch-processing]
chapter: Ch10
---

# Dataflow Engines

**Definition:** Frameworks (Spark, Tez, Flink) that generalize beyond MapReduce's rigid map-then-reduce structure into flexible operator graphs, often keeping intermediate state in memory.

**Why it matters:** Avoid much of MapReduce's overhead, like unnecessary materialization to disk between every step, making multi-stage jobs significantly faster.

**Example:** A Spark job expressed as a DAG of `filter -> map -> join -> aggregate` stages, each piped directly into the next without ever hitting disk in between.

**Related:** [[MapReduce]] [[Join Algorithms]]
