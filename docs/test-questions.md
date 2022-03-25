# Questions for the microservices class

## Introduction

1. What from the following are benefits of writing monolithic apps (select 3):

- [x] Simple and comfortable development
- [x] Single code base
- [x] Simple testing and deployment
- [ ] Rich user interface
- [ ] Built on top of technologies and frameworks which are hard to change

2. What of the following is functional decomposition? 

- [x] Split of the code based on its functions
- [ ] Split of data and adding multiple instances of the app for every shard
- [ ] Running multiple instances of the application and putting them behind the load balancer

3. What of the following is relevant to the service-oriented architecture (select 3):

- [x] Usage of the enterprise service bus (ESB) or SOAP
- [x] Global or shared database
- [x] Applications are small but strongly coupled
- [ ] Every service has its own database
- [ ] Applications are small and independent

## Decomposition strategies

1. What views are included into 4+1 model (select 5):

- [x] Logical view
- [x] Implementation view
- [x] Deployment view
- [x] Process view
- [x] Scenarios
- [ ] Sequence view
- [ ] Activity view
- [ ] State view

2. What of the following are quality attributes (select 3):

- [x] Performance
- [x] Security
- [x] Observability
- [ ] Functions that an application should perform
- [ ] Color of buttons of the user interface

3. What of the following are characteristics of the hexagonal architecture (select 3):

- [x] Logical view is organized in a way that places the business logic at the centre
- [x] Inbound adapters are handling requests from the outside by invoking business logic
- [x] A port defines a set of operations and how business logic interacts with external services
- [ ] Presentation layer contains code that implements the user interface or external API
- [ ] Persistance layer contains the logic of interacting with a database


4. ... is a standalone, independently deployable software component that implements some functionality

- [x] Service
- [ ] Application
- [ ] Provider
- [ ] API
- [ ] OSGi bundle

5. What is a system operation? 

- [x] An abstraction of a request that the service must handle
- [ ] Way of collaboration between services
- [ ] Operations with underlying file system or database
- [ ] Operations that involve multiple services

6. What of the following system operations are commands (select 3):

- [x] Operations that create data
- [x] Operations that update data
- [x] Operations that delete data
- [ ] Operations that query data
- [ ] Events

7. What are goals of domain-driven design (select 3):

- [x] Placing the project's primary focus on the core domain and domain logic
- [x] Basing complex designs on a model of the domain
- [x] Initiating a creative collaboration between technical and domain experts to iterative refine a conceptual model that addresses particular domain problems
- [ ] Using inbound and outbound ports and adapters to separate business logic from UI and storage
- [ ] Separation of modules based on business capabilities

8. What principle is described below: 

```
The classes in a package should be closed together against the same kinds of changes. A change that affects a package affects all the classes in the package. 
```

- [x] Common Closure Principle
- [ ] Single Responsibility Principle
- [ ] Common Reuse Principle
- [ ] The Acyclic Dependencies Principle
- [ ] Dependency Inversion Principle

9. What of the following are obstacles to decomposing applications into services (select 3):

- [x] Network latency
- [x] Reduced availability 
- [x] Maintaining data consistency across services
- [ ] Small size of resulting applications
- [ ] Increasing code complexity due to using frameworks

## Inter-process communication

1. What communication style assumes that the response will arrive in a timely manner: 

- [x] Request/response
- [ ] One-way notification
- [ ] Publish/subscribe
- [ ] Asynchronous request/response

2. What of the following are characteristics of API (select 3):

- [x] Inter-process communication mechanism
- [x] Defined using interface definition language (IDL)
- [x] Defines a contract for communication
- [ ] Will not be changed over time
- [ ] Written in one single programming language

3. What is semantic versioning specification? 

- [x] Guide to versioning API, set of rules that specify how version number are used
- [ ] Guide to versioning API, set of rules that specify how deprecation is happening
- [ ] Guide to versioning API that says that every version should have its own endpoint
- [ ] Guide to versioning API that says that headers should be introduced

4. What of the following are backward-compatible changes (select 3):

- [x] Adding optional attributes to request
- [x] Adding attributes to response
- [x] Adding new operations
- [ ] Removing optional attributes from request
- [ ] Adding mandatory attributes to request

5. What of the following are binary message formats (select 3):

- [x] Protocol Buffers
- [x] Thrift
- [x] Avro
- [ ] JSON
- [ ] XML

6. In accordance with the REST maturity model, what is relevant for the level 2?

- [x] Different HTTP requests for different actions
- [ ] HTTP POST requests to its sole URL endpoint
- [ ] Resources are introduced, clients make POST requests to resource endpoints
- [ ] HATEOAS, Hypertext As The Engine Of Application State

7. What of the following are benefits of gRPC (select 3):

- [x] Supports multiple update operations
- [x] Compact IPC mechanism
- [x] Supports bidirectional data streaming
- [ ] Human-readable message format
- [ ] Works on top of HTTP/1

8. What of the following help developing robust RPI proxies (select 3):

- [x] Use network timeouts
- [x] Limit number of requests from clients to services
- [x] Use circuit breaker pattern
- [ ] Use binary message formats
- [ ] Return errors to clients

9. What are characteristics of the application-level service discovery (select 3):

- [x] Self registration pattern
- [x] Client-side discovery pattern
- [x] Heartbeat
- [ ] DNS
- [ ] vIP

10. What are characteristics of the platform-provided service discovery (select 3):

- [x] 3-rd party registration pattern
- [x] Client-side discovery pattern
- [x] DNS
- [ ] Service discovery application
- [ ] Load balancing on the client side

11. What of the following are message kinds in the async communication way (select 3):

- [x] Document
- [x] Command
- [x] Event
- [ ] Query
- [ ] Request

12. What should be included into the message in order to implement async request/response communication model (select 3):

- [x] Message identifier
- [x] Correlation ID
- [x] Reply channel
- [ ] JSON body
- [ ] Processing status

13. What are benefits of using broker-based messaging architecture (select 3):

- [x] Message buffering
- [x] Loose coupling
- [x] Explicit inter-process communication
- [ ] Additional operational complexity
- [ ] Better latency
- [ ] Lower network traffic

14. What of the following helps to achieve single message processing? 

- [x] Transaction table
- [ ] Outbox table
- [ ] Transaction log
- [ ] Message ordering

15. What of the following helps to achieve reliable sending of messages? 

- [x] Outbox table pattern
- [ ] Transaction log
- [ ] Message ordering
- [ ] Transaction table

## Managing transactions with Saga pattern

1. What of the following are characteristics of transactions (select 4):

- [x] Atomicity
- [x] Consistency
- [x] Independency
- [x] Durability
- [ ] Reliability
- [ ] Repeatability
- [ ] Performance

2. What should be taken into account while designing distributed systems (select 3):

- [x] Consistency
- [x] Availability
- [x] Partition tolerance
- [ ] Consistency
- [ ] Durability

3. What transaction types are considered by Saga pattern (select 3): 

- [x] Pivot transactions
- [x] Compensation transactions
- [x] Retriable transactions
- [ ] Forward transactions
- [ ] Backward-compatible transactions

4. In case of distributed transaction, what of the following is handled by the local database? (select 2) 

- [x] Durability
- [x] Consistency
- [ ] Atomicity
- [ ] Independency

5. What of the following anomalies are led by using the saga pattern (select 3):

- [x] Lost updates
- [x] Dirty reads
- [x] Fuzzy/non-repeatable reads
- [ ] Transactions serialization
- [ ] Transaction intersection

6. What counter measure allows to prevent dirty reads by re-reading data before writing? 

- [x] Reread value
- [ ] Pessimistic view
- [ ] Version file
- [ ] Semantic lock
- [ ] Commutative updates

## Designing business logic

1. What of the following DDD pattern is used to store collection values: 

- [x] Value object
- [ ] Entity
- [ ] Factory
- [ ] Repository
- [ ] Service

2. What of the following are characteristics of the aggregates? (select 3)

- [x] Aggregates are consistency boundaries
- [x] Aggregates are referenced by key only
- [x] References between aggregates are by their primary keys only
- [ ] It's possible to reference internal object
- [ ] Transactions can create or update multiple aggregates