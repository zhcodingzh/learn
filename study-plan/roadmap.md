# Eight-Week Senior Java Interview Roadmap

Updated: 2026-07-20

The complete topic inventory is in [High-Frequency Master Plan](high-frequency-master-plan.md). This roadmap determines execution order.

## Continuous work every week

Every week must include:

- one resume/project story;
- English technical answers;
- spaced review;
- at least one coding or SQL exercise;
- one mixed mock or mini-mock.

## Week 1 — Concurrency and Spring baseline

- Visibility, atomicity and ordering
- Locks and concurrent collections
- ThreadPoolExecutor
- CompletableFuture and three-API aggregation
- Spring IoC, `@Async`, starters and startup behaviour
- Closed-book assessment

## Week 2 — Spring core and transactions

- Bean lifecycle and scopes
- AOP, JDK proxy and CGLIB
- Self-invocation problems
- Spring MVC request flow
- Auto-configuration and conditional annotations
- `@Transactional` mechanism
- Propagation, isolation and rollback failure cases
- Spring testing

## Week 3 — Java core, collections and JVM

- String and immutability
- `equals()` / `hashCode()`
- HashMap and ConcurrentHashMap
- ArrayList, LinkedList and common collections
- Exceptions, generics and streams
- Java Memory Model and happens-before
- JVM memory areas, class loading and GC
- Production JVM troubleshooting

## Week 4 — SQL, JPA, Redis and messaging

- Indexes and execution plans
- ACID, isolation, MVCC and locks
- Slow queries and pagination
- JPA fetching and N+1
- Connection pools
- Cache-aside and cache failure modes
- Cache/database consistency
- Idempotency and distributed locks
- Message delivery, duplicate consumption and outbox

## Week 5 — REST, security and microservices

- REST semantics and idempotency
- API errors, validation and versioning
- JWT and Spring Security
- Gateway and service discovery
- Timeout, retry, circuit breaker and bulkhead
- Rate limiting
- Saga and eventual consistency
- Distributed tracing

## Week 6 — System design, Kubernetes and observability

- Requirement and capacity clarification
- Payment/order design
- External-API aggregation design
- Scaling, sharding and caching
- Failure recovery and security
- Kubernetes core objects
- Readiness/liveness, rolling deployment and rollback
- Logs, metrics, traces and alerting

## Week 7 — Coding and project deep dives

- Arrays, strings and hash maps
- Two pointers and sliding window
- Stack, queue, linked list and binary search
- Tree/graph traversal and heap
- SQL coding
- Thread-safe coding
- OTT Pay and insurance project stories
- Production-incident STAR stories

## Week 8 — Full English interview simulation

- Java/Spring mock
- Database/concurrency mock
- Microservices/system-design mock
- Project/behavioural mock
- Repair repeated mistakes
- Final 30/90/180-second English answer set
- JD-specific P1/P2 review

## Weekly rhythm

| Day | Focus |
|---|---|
| Monday | Due review + new P0 topic |
| Tuesday | Due review + code/SQL |
| Wednesday | English answer + new P0 topic |
| Thursday | Mixed follow-ups + project connection |
| Friday | Project and behavioural stories |
| Saturday | 45–60 minute mock |
| Sunday | Progress update and next-week queue |

## Scheduling rule

Do not wait for one domain to become perfect before touching another. Learn in focused blocks but use mixed spaced review so earlier material remains retrievable.
