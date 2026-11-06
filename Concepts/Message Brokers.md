---
tags: [ddia, stream-processing]
chapter: Ch11
---

# Message Brokers

**Definition:** Middleware (e.g. RabbitMQ) that lets producers send messages to consumers asynchronously, decoupling them in time, typically deleting a message once it's been acknowledged.

**Why it matters:** Provides a flexible way to connect producers and consumers that run at different speeds, with the broker handling buffering.

**Example:**

```mermaid
flowchart LR
  P[Producer] --> MB[[Broker queue]] --> C[Consumer]
```
Once consumed and acked, the message is gone from the queue.

**Related:** [[Log-Based Message Brokers]] [[Event Streams]]
