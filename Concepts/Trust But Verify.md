---
tags: [ddia, future-architecture]
chapter: Ch12
---

# Trust But Verify

**Definition:** The practice of adding runtime auditing and integrity checks to a data system instead of assuming its correctness, so corruption or bugs can be detected after the fact.

**Why it matters:** Reflects the book's broader call for stronger end-to-end correctness checking, given how easily subtle bugs or hardware faults can silently corrupt data.

**Example:** A nightly job that recomputes checksums over stored files and alerts if any differ from what was written — catching silent bit-rot instead of assuming disks never lie.

**Related:** [[End-to-End Argument]]
