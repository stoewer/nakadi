# Table of Contents 
* [Getting Started](getting-started.md)
* [FAQ](faq.md)
* [Using Nakadi](using.md)
  - [Concepts](using/concepts.md)
  - [Event Types](using/event-types.md)
  - [Producing Events](using/producing-events.md)
  - [Consuming Events (Low-level API)](using/consuming-events-lola.md)
  - [Consuming Events (High-level API)](using/consuming-events-hila.md)
  - [Per-Event Type Authorization](using/authorization.md)
  - [Client Libraries](using/clients.md)
  - [(partial) Compared to Other Systems](using/comparison.md)
* [API Reference](api-spec-generated/overview.md)
  - [Paths](api-spec-generated/paths.md)
  - [Definitions](api-spec-generated/definitions.md)
  - [Security](api-spec-generated/security.md)
* [Building and Developing](developing.md)
* [(todo) Operations](operating.md)
* [(todo) Recipes and Patterns](recipes.md)

# Nakadi Reference Manual


**[Nakadi](https://github.com/zalando/nakadi)** is a distributed, open-source event broker under development at [Zalando](https://zalando.github.io/). It is [available on GitHub](https://github.com/zalando/nakad

### Why Nakadi?

The goal of Nakadi is to enable convenient development of event-driven applications and asynchronous microservices by allowing producers to publish streams of event data to multiple consumers, without direct int

Operations is also a factor behind Nakadi's design. Managing upgrades to systems like Kafka becomes easier when technology sits behind an API and isn't a shared dependency between microservices. Asychronous even

The section ["Comparison to Other Systems"](https://github.com/zalando-nakadi/nakadi-manual/blob/master/docs/using/comparison.md) describes Nakadi relative to systems such as Apache Kafka, AWS Kinesis, Google Pu

### Features

- **A secured HTTP API.** This allows microservices teams to maintain service boundaries, and not directly depend on any specific message broker technology. Access to the API can be managed and secured using OAu

- **An event type registry.** Events sent to Nakadi can be defined with a schema and managed via a registry. Events can be validated before they are distributed to consumers.
.
- **Inbuilt event types.** Nakadi also has optional support for events describing business processes and data changes using standard primitives for identity, timestamps, event types, and causality..

-  **Low latency event delivery.** Once a publisher sends an event using a simple HTTP POST, consumers can be pushed to via a streaming HTTP connection, allowing near real-time event processing. The consumer con

- **Compatibility with the [STUPS project](https://stups.io/).** STUPS is Zalando's open source platform infrastructure for running and securing microservices on AWS.

- **Built on proven infrastructure.** Nakadi uses the excellent [Apache Kafka](http://kafka.apache.org/) as its internal message broker and the also excellent PostgreSQL as a backing database..

### Roadmap Note: Upcoming Features

#### Subscription API

The [API reference](http://zalando.github.io/nakadi-manual/docs/api-spec-generated/overview.html) focuses on the existing core API. The project is also planning a higher level _subscription API_.  The details ar

 - Basic functionality for supporting consumer groups via a subscription.
 - Server managed and persisted checkpointing of partition cursors.
 - Server managed rebalancing of partitions on behalf of consumers.



