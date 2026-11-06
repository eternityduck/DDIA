---
tags: [ddia, data-models]
chapter: Ch2
---

# Normalization

**Definition:** Removing duplication in relational data by extracting repeated values into separate tables referenced by ID (e.g. extracting 'region' into its own table).

**Why it matters:** Avoids inconsistency bugs from duplicated data, at the cost of requiring joins to reassemble it.

**Example:** Storing `region_id` + a separate `regions` table instead of repeating the string "Europe/Warsaw" in every row.

**Related:** [[Relational Model]] [[Impedance Mismatch]]
