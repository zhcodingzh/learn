# Senior Java Interview — High-Frequency Master Plan

Updated: 2026-07-20

This is the authoritative topic list. Voice sessions should follow this priority order instead of asking which topic to study.

## Priority definitions

- **P0 — Must master:** appears repeatedly across Senior Java interviews or is essential for defending real project experience. Target mastery: Level 4–5.
- **P1 — Frequently asked:** common follow-up or role-dependent topic. Target mastery: Level 3–4.
- **P2 — Bonus / JD-dependent:** useful after P0 and P1, or when a job description explicitly requires it. Target mastery: Level 2–3.

A topic is not complete until it can be explained without notes, answered in English, handled under follow-up questions and connected to code or a project.

---

## P0: Immediate interview priorities

### 1. Resume, self-introduction and project deep dives

- [ ] 60-second English self-introduction
- [ ] 2–3 minute Senior Java profile
- [ ] OTT Pay OMS architecture and personal contribution
- [ ] Transactions, Finance, Reconciliation, Risk and Resources integration
- [ ] Risk rules, disputes, settlement cycles and rolling reserve changes
- [ ] Taikang high-concurrency incident: symptom, diagnosis, fix and result
- [ ] Nginx logs and Hystrix tuning story
- [ ] 24 Tomcat instances and scaling architecture
- [ ] Sharding migration from modulo 8 to modulo 9
- [ ] Kubernetes readiness/liveness and production troubleshooting
- [ ] SonarQube high-risk issue remediation
- [ ] One conflict/failure/lesson story using STAR
- [ ] “What would you improve now?” for every major project

### 2. Java core and collections

- [ ] OOP principles with practical examples
- [ ] Interface vs abstract class
- [ ] Immutability and why String is immutable
- [ ] String pool, literals, `new String()` and `intern()`
- [ ] `==` vs `equals()`
- [ ] `equals()` and `hashCode()` contract
- [ ] HashMap hashing, buckets and collision handling
- [ ] HashMap resize threshold, load factor and 2x capacity growth
- [ ] Linked-list to red-black-tree conversion
- [ ] Why HashMap is not thread-safe
- [ ] ArrayList growth and random access
- [ ] ArrayList vs LinkedList trade-offs
- [ ] HashSet implementation
- [ ] Comparable vs Comparator
- [ ] Checked vs unchecked exceptions
- [ ] `throw` vs `throws`
- [ ] Generic type erasure and bounded types
- [ ] Stream lazy evaluation, intermediate and terminal operations
- [ ] `map()` vs `flatMap()`
- [ ] Optional: correct use and misuse
- [ ] Deep copy vs shallow copy

### 3. Concurrency and Java Memory Model

- [x] Visibility vs mutual exclusion vs task coordination — discussed
- [x] `volatile` visibility and non-atomic compound operations — discussed
- [ ] happens-before rules
- [ ] atomicity, visibility and ordering
- [ ] `synchronized`: monitor, reentrancy and memory guarantees
- [ ] `ReentrantLock` vs `synchronized`
- [x] `ReentrantReadWriteLock` — discussed, needs recall
- [x] `StampedLock` optimistic read and validation — discussed, needs recall
- [ ] Deadlock conditions, prevention and diagnosis
- [ ] Race condition and safe publication
- [ ] `AtomicInteger`, CAS and retry loop
- [x] ABA problem — discussed, needs recall
- [ ] `LongAdder` vs `AtomicLong`
- [x] ConcurrentHashMap safety and CAS — discussed, needs recall
- [x] `compute()` vs `computeIfAbsent()` — discussed, needs recall
- [x] `CountDownLatch` — discussed, needs recall
- [ ] Semaphore, CyclicBarrier and Phaser use cases
- [ ] Thread states and interruption
- [x] ThreadPoolExecutor core parameters — discussed, needs recall
- [ ] Task submission sequence and queue behavior
- [ ] Rejection policies
- [x] `shutdown()`, `shutdownNow()` and `awaitTermination()` — discussed
- [ ] CPU-bound vs I/O-bound pool sizing
- [x] CompletableFuture composition — discussed, needs stronger recall
- [ ] `thenApply()`, `thenCompose()`, `thenCombine()`, `allOf()`
- [ ] Timeout, exception, cancellation and partial-success policies
- [ ] Dedicated executor vs common ForkJoinPool
- [ ] Three-external-API aggregation design

### 4. JVM, memory and garbage collection

- [x] Stack, heap and GC Roots — discussed, needs recall
- [ ] JVM runtime memory areas
- [ ] Stack frame, local variables and method invocation
- [ ] Object allocation and escape analysis
- [ ] Strong, soft, weak and phantom references
- [ ] Reachability analysis and GC Roots
- [ ] Young/old generations and object promotion
- [ ] Minor GC, major GC and full GC
- [ ] Stop-the-world
- [ ] Serial, Parallel, CMS, G1 and ZGC overview
- [ ] G1 regions and pause-time goal
- [ ] Class loading phases and parent delegation
- [ ] Metaspace vs permanent generation
- [ ] OOM types and likely causes
- [ ] Memory leak vs memory exhaustion
- [ ] Reading GC logs
- [ ] Heap dump, thread dump, `jstack`, `jmap` and `jcmd`
- [ ] High CPU, deadlock and memory troubleshooting process

### 5. Spring and Spring Boot

- [x] IoC and dependency injection — discussed
- [ ] Constructor injection vs field injection
- [ ] Bean scopes
- [ ] Complete Bean lifecycle
- [ ] How Spring resolves circular dependencies and its limitations
- [ ] AOP proxy mechanism
- [ ] JDK dynamic proxy vs CGLIB
- [ ] Why self-invocation can bypass proxy-based annotations
- [ ] Spring MVC request lifecycle
- [ ] Filter vs Interceptor vs AOP
- [ ] Spring Boot auto-configuration mechanism
- [ ] Conditional annotations
- [x] Starter dependencies — discussed, needs recall
- [x] Lazy initialization and first-request trade-off — discussed
- [ ] Configuration properties and profiles
- [ ] Global exception handling
- [ ] Validation
- [x] `@Async` external-call/proxy requirement — discussed, needs recall
- [ ] `@Transactional` proxy mechanism
- [ ] Transaction propagation: REQUIRED, REQUIRES_NEW and NESTED
- [ ] Transaction isolation
- [ ] Common transaction failure scenarios
- [ ] Rollback rules for checked and unchecked exceptions
- [ ] Spring Security authentication vs authorization
- [ ] JWT flow, expiration and refresh strategy
- [ ] Testing: unit, slice and integration tests
- [ ] Mockito, MockMvc and Testcontainers

### 6. SQL and database

- [ ] B-tree/B+tree index principles
- [ ] Clustered vs non-clustered indexes
- [ ] Composite index and leftmost-prefix rule
- [ ] Covering index
- [ ] When an index is not used
- [ ] Reading an execution plan
- [ ] Slow-query diagnosis
- [ ] ACID
- [ ] Isolation levels and anomalies
- [ ] MVCC
- [ ] Optimistic vs pessimistic locking
- [ ] Deadlocks and lock ordering
- [ ] Pagination performance
- [ ] N+1 query problem
- [ ] JPA entity lifecycle and fetching
- [ ] Lazy vs eager loading
- [ ] Transaction boundaries
- [ ] Read/write splitting and replication lag
- [ ] Sharding key selection and resharding
- [ ] Database connection pool sizing

### 7. REST API, microservices and distributed systems

- [ ] REST constraints and resource-oriented API design
- [ ] HTTP methods, idempotency and status codes
- [ ] API versioning and backward compatibility
- [ ] Pagination, filtering and sorting
- [ ] Request validation and error response design
- [ ] Authentication, authorization, TLS and CORS
- [ ] Service discovery and configuration management
- [ ] API Gateway responsibilities
- [ ] Synchronous vs asynchronous communication
- [ ] Timeout budget
- [ ] Retry with backoff and jitter
- [ ] Circuit breaker
- [ ] Bulkhead and rate limiting
- [ ] Fallback and graceful degradation
- [ ] Distributed tracing and correlation IDs
- [ ] Idempotency keys
- [ ] Distributed transaction challenges
- [ ] Saga pattern
- [ ] Eventual consistency
- [ ] CAP theorem and practical trade-offs
- [ ] Duplicate request and duplicate message handling
- [ ] Partial failure and compensation

### 8. Redis, caching and messaging

- [ ] Redis core data structures and use cases
- [ ] Cache-aside pattern
- [ ] Cache penetration, breakdown and avalanche
- [ ] Cache consistency with database
- [ ] TTL design and randomization
- [ ] Hot keys and big keys
- [ ] Redis persistence: RDB vs AOF
- [ ] Redis replication and cluster overview
- [ ] Distributed locks and ownership-safe unlock
- [ ] Redlock: purpose and controversy at a high level
- [ ] Idempotency with Redis
- [ ] Message queue use cases
- [ ] At-most-once, at-least-once and exactly-once semantics
- [ ] Producer retry and consumer retry
- [ ] Duplicate consumption
- [ ] Ordering
- [ ] Dead-letter queue
- [ ] Outbox pattern
- [ ] Consumer lag and backpressure

### 9. System design

- [ ] Requirement clarification and capacity assumptions
- [ ] High-level component diagram
- [ ] API and data model
- [ ] Load balancing and horizontal scaling
- [ ] Database selection and sharding
- [ ] Caching
- [ ] Consistency and transaction boundaries
- [ ] Failure modes and recovery
- [ ] Security
- [ ] Observability
- [ ] Cost and trade-offs
- [ ] Design a payment/order system
- [ ] Design an API aggregation service
- [ ] Design an idempotent payment endpoint
- [ ] Design notification processing
- [ ] Design rate limiting
- [ ] Design an audit/risk-rule platform

### 10. Coding and problem solving

- [ ] Big-O time and space complexity
- [ ] Arrays and strings
- [ ] Hash map/set problems
- [ ] Two pointers
- [ ] Sliding window
- [ ] Stack and queue
- [ ] Linked list
- [ ] Binary search
- [ ] Tree traversal: BFS and DFS
- [ ] Heap / priority queue
- [ ] Basic graph traversal
- [ ] Recursion and backtracking
- [ ] Common dynamic-programming patterns
- [ ] Thread-safe coding exercise
- [ ] SQL query exercise
- [ ] Clean code, naming, tests and edge cases

### 11. Behavioural and English communication

- [ ] Tell me about yourself
- [ ] Most challenging production issue
- [ ] Disagreement with a teammate
- [ ] Missed deadline or failure
- [ ] Mentoring and code review
- [ ] Working with ambiguous requirements
- [ ] Prioritization under pressure
- [ ] Improving performance or reliability
- [ ] Security or quality improvement
- [ ] Why this company and why this role
- [ ] Why are you looking for a new position?
- [ ] Strengths and development areas
- [ ] STAR structure without excessive detail
- [ ] 30/90/180-second versions of technical answers
- [ ] Clarifying questions when the interviewer is unclear

---

## P1: Frequently asked follow-ups

### Design patterns and engineering practices

- [ ] SOLID principles
- [ ] Strategy, Factory, Builder, Adapter, Observer and Template Method
- [ ] Singleton risks and Spring singleton scope
- [ ] Dependency inversion
- [ ] Clean architecture and separation of concerns
- [ ] Domain-driven design basics
- [ ] Code review approach
- [ ] Refactoring legacy code
- [ ] Feature flags
- [ ] Backward-compatible database migration
- [ ] Logging without leaking sensitive data

### DevOps, Kubernetes and observability

- [ ] Docker image and container concepts
- [ ] Kubernetes Pod, Deployment, Service, ConfigMap and Secret
- [x] Readiness vs liveness — discussed, needs project answer
- [ ] Resource requests and limits
- [ ] Horizontal Pod Autoscaler
- [ ] Rolling deployment and rollback
- [ ] Kubernetes service discovery vs Eureka
- [x] Spring Cloud components and Kubernetes overlap — discussed
- [ ] CI/CD pipeline stages
- [ ] Blue-green vs canary deployment
- [ ] Logs, metrics and traces
- [ ] SLI, SLO and alerting
- [ ] Prometheus metric types
- [ ] ELK troubleshooting flow

### Testing

- [ ] Unit vs integration vs end-to-end tests
- [ ] Test pyramid
- [ ] Mocking boundaries
- [ ] Contract testing
- [ ] Testcontainers
- [ ] Concurrency testing
- [ ] Performance/load testing
- [ ] Avoiding flaky tests

---

## P2: JD-dependent or bonus topics

- [ ] Java records, sealed classes and pattern matching
- [ ] Virtual threads and structured-concurrency concepts
- [ ] Reactive programming and Spring WebFlux
- [ ] Native image / AOT concepts
- [ ] Kafka partition, offset, consumer group and rebalance details
- [ ] OAuth 2.0 and OpenID Connect details
- [ ] Cloud-specific services for AWS, Azure or GCP
- [ ] GraphQL
- [ ] gRPC
- [ ] NoSQL data modelling
- [ ] WCF concepts when explicitly mentioned by a job description
- [ ] Front-end basics only when required by the role

---

## Mandatory learning order

1. Project stories and self-introduction
2. Spring/Spring Boot transactions, AOP and lifecycle
3. Java concurrency and thread pools
4. SQL indexes and transactions
5. Java core collections
6. JVM and production troubleshooting
7. REST/microservices resilience
8. Redis and messaging
9. System design
10. Coding practice
11. Kubernetes/observability
12. P1 and JD-specific P2 topics

The order is deliberately weighted toward Senior-level interviews and the user's real experience, not textbook chapter order.
