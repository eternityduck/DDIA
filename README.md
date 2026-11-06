# DDIA — Designing Data-Intensive Applications Notes

An [Obsidian](https://obsidian.md) vault of notes on Martin Kleppmann's *Designing Data-Intensive Applications*. Every concept gets its own note, linked back to the book part it belongs to, so the whole thing doubles as a personal knowledge graph of the book.

```mermaid
flowchart LR
    Index["📖 00-Index"]

    Index --> P1["Part 1\nFoundations of Data Systems\n(34 concepts)"]
    Index --> P2["Part 2\nDistributed Data\n(44 concepts)"]
    Index --> P3["Part 3\nDerived Data\n(16 concepts)"]

    P1 --> P1a["Reliability · Scalability · Maintainability"]
    P1 --> P1b["Data models: Relational · Document · Graph"]
    P1 --> P1c["Storage: B-Trees · LSM-Trees · SSTables"]
    P1 --> P1d["Encoding: Protobuf · Thrift · Avro"]

    P2 --> P2a["Replication: Leader · Multi-Leader · Leaderless"]
    P2 --> P2b["Partitioning: Hash · Key Range · Rebalancing"]
    P2 --> P2c["Transactions: ACID · Isolation Levels · 2PL"]
    P2 --> P2d["Consensus: Paxos · Raft · CAP · Linearizability"]

    P3 --> P3a["Batch: MapReduce · Dataflow Engines"]
    P3 --> P3b["Streaming: Event Sourcing · CDC · Exactly-Once"]
    P3 --> P3c["Architecture: Lambda · Unbundling Databases"]

    style Index fill:#4c6ef5,color:#fff
    style P1 fill:#2b8a3e,color:#fff
    style P2 fill:#e8590c,color:#fff
    style P3 fill:#9c36b5,color:#fff
```

## Structure

| Part | Topic | Concepts |
|---|---|---|
| [Part 1](<Part 1 - Foundations of Data Systems.md>) | Foundations of Data Systems | 34 |
| [Part 2](<Part 2 - Distributed Data.md>) | Distributed Data | 44 |
| [Part 3](<Part 3 - Derived Data.md>) | Derived Data | 16 |

Each part note is a map of content (MOC) linking out to the individual concept notes in [`Concepts/`](Concepts). Every concept note follows the same [template](<Templates/Concept Template.md>): definition, why it matters, related concepts, and book location.

Start at [`00-Index.md`](00-Index.md).

## Usage

Clone the repo and open the folder as a vault in Obsidian to get clickable `[[wikilinks]]` and the graph view. The notes also render fine as plain Markdown on GitHub.
