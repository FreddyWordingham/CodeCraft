# 🔗 CAP Theorem

In database theory, the CAP theorem, also named Brewer's theorem after computer scientist Eric Brewer, states that any distributed data store can provide only two of the following three guarantees:

- **Consistency**
  Every read receives the most recent write or an error.
- **Availability**
  Every request received by a non-failing node in the system must result in a response. Note that availability as defined in CAP theorem is different from high availability in software architecture.
- **Partition tolerance**
  The system continues to operate despite an arbitrary number of messages being dropped (or delayed) by the network between nodes.

When a network partition failure happens, it must be decided whether to do one of the following:

- Cancel the operation and thus decrease the availability but ensure consistency
- Proceed with the operation and thus provide availability but risk inconsistency.

> Note this doesn't necessarily mean that system is highly available to its users.

[CAP theorem Euler diagram](https://en.wikipedia.org/wiki/CAP_theorem#/media/File:CAP_Theorem_Venn_Diagram.png)

Thus, if there is a network partition, one has to choose between consistency or availability. Note that consistency as defined in the CAP theorem is quite different from the consistency guaranteed in ACID database transactions.

## Trade-offs

Understanding the Trade-offs

- **CA (Consistency and Availability)**: Achieving both consistency and availability is possible only when there are no network partitions. However, in a real-world scenario, network failures are inevitable, so this combination is impractical for distributed systems.
- **CP (Consistency and Partition Tolerance)**: In the presence of network partitions, the system will sacrifice availability to maintain consistency. This means that some requests might be denied or delayed until the system can ensure a consistent state.
- **AP (Availability and Partition Tolerance)**: The system remains available even during network partitions, but it might return outdated or inconsistent data to ensure availability.

**Practical Examples**

- **CA Systems**: Traditional relational databases (when operating in a non-distributed, single-node setup).
- **CP Systems**: Distributed databases like HBase or MongoDB (when configured to prioritise consistency).
- **AP Systems**: DynamoDB, Couchbase, Cassandra (focus on availability and partition tolerance, allowing for eventual consistency).
