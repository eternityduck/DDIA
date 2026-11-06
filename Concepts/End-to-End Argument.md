---
tags: [ddia, future-architecture]
chapter: Ch12
---

# End-to-End Argument

**Definition:** The principle that certain correctness guarantees, like exactly-once effects or duplicate suppression, can only be reliably implemented at the application (end-to-end) level, since lower network layers can't fully solve it on an application's behalf.

**Why it matters:** Explains why techniques like idempotency keys are needed at the application layer even when the transport layer offers its own reliability guarantees.

**Example:** A flaky mobile network retries a payment request 3 times at the TCP level — only an application-level idempotency key actually prevents the user being charged 3 times.

**Related:** [[Exactly-Once Semantics]]
