---
tags: [ddia, foundations]
chapter: Ch1
---

# Reliability

**Definition:** The system continues to work correctly (performing the correct function at the desired level of performance) even in the face of adversity: hardware faults, software bugs, or human error.

**Why it matters:** Forms one of the three core concerns (with scalability and maintainability) that should guide the design of any data system.

**Example:** Netflix's Chaos Monkey deliberately kills production servers to verify reliability assumptions actually hold, instead of just hoping they do.

**Related:** [[Fault vs Failure]] [[Scalability]]
