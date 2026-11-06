---
tags: [ddia, transactions]
chapter: Ch7
---

# Atomicity

**Definition:** A transaction either fully commits (all its writes take effect) or fully aborts (none do); there is no partial-failure state visible to other transactions.

**Why it matters:** Lets application code safely retry failed transactions, knowing partial effects won't linger.

**Example:** If step 3 of a 5-step transaction fails, steps 1-2 are rolled back as if none of it ever happened — the application can safely just retry.

**Related:** [[ACID]] [[Two-Phase Commit]]
