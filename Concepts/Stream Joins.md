---
tags: [ddia, stream-processing]
chapter: Ch11
---

# Stream Joins

**Definition:** Joining a stream with another stream, or with a changing table, over a window of time, since unlike batch there is no fixed, complete dataset to join against.

**Why it matters:** Needed for enriching events (e.g. joining clicks with user profile data) in real time, but fundamentally harder than a batch join because inputs never 'finish.'

**Example:** Enriching a `PageViewed` event stream with each user's current `country` from a slowly-changing users table, re-joined as that table updates.

**Related:** [[Stream Processing Windows]] [[Dataflow Engines]]
