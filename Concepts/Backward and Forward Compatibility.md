---
tags: [ddia, encoding]
chapter: Ch4
---

# Backward and Forward Compatibility

**Definition:** Backward compatibility means newer code can read data written by older code; forward compatibility means older code can read data written by newer code.

**Why it matters:** Needed for rolling upgrades, where old and new code (and old and new data) run simultaneously.

**Example:** New code adds a field with a default — old code (forward compat) ignores it; old data without the field still parses in new code (backward compat).

**Related:** [[Schema Evolution]]
