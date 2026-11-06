---
tags: [ddia, stream-processing]
chapter: Ch11
---

# Stream Processing Windows

**Definition:** Grouping events for aggregation by time windows (tumbling, hopping, sliding) or session windows, defined either by arrival (processing) time or by the event's own timestamp.

**Why it matters:** Handling out-of-order and straggler events correctly, i.e. event-time vs processing-time windows, is one of the hardest parts of correct stream processing.

**Example:**

```
|--- window 1 (0-60s) ---|--- window 2 (60-120s) ---|
   e1  e2    e3              e4   e5
```
An event from second 58 that arrives late at second 65 is a straggler the window logic must handle.

**Related:** [[Stream Joins]] [[Event Streams]]
