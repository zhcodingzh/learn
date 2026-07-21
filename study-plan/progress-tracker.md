# Progress Tracker

Updated: 2026-07-20

All levels below are estimates until verified by closed-book recall and English follow-up questions.

## Current position

**Current learning focus:** Spring Boot / Spring Framework high-frequency questions  
**Parallel review focus:** Java concurrency and asynchronous programming  
**Next mandatory topic:** Spring transactions, AOP proxy behaviour and Bean lifecycle

## Domain status

| Domain | Status | Estimated level | Immediate next action |
|---|---|---:|---|
| Resume/project stories | Needs structure | 1–2 | Build self-introduction and two project deep dives |
| Java core/collections | Started | 2–3 | Closed-book HashMap and equals/hashCode review |
| Concurrency/JMM | Actively studied | 2–3 | Mixed recall plus English answers |
| Thread pools/async | Actively studied | 2 | Verify executor flow, shutdown and CompletableFuture |
| JVM/GC | Started | 2 | Review memory areas, GC Roots and GC process |
| Spring/Spring Boot | Current topic | 1–2 | Transactions, AOP, lifecycle and auto-configuration |
| SQL/database | Not recently verified | 1–2 | Index and isolation-level baseline |
| Redis/MQ | Partial project exposure | 1–2 | Cache and idempotency baseline |
| Microservices | Strong experience, theory needs structure | 2–3 | Resilience patterns and distributed consistency |
| Kubernetes/observability | Project experience | 2–3 | Convert experience into interview answers |
| System design | Needs structured practice | 1–2 | Payment/API aggregation design |
| Coding/algorithms | Not assessed | 0–1 | Baseline coding test |
| Behavioural English | Needs systematic preparation | 1–2 | STAR story bank |

## Topics already discussed but requiring spaced review

- `volatile`, atomicity, visibility and ordering
- `synchronized`
- `ReentrantReadWriteLock`
- `StampedLock`
- `CountDownLatch`
- `ConcurrentHashMap`
- CAS and ABA
- `compute()` and `computeIfAbsent()`
- `ThreadPoolExecutor` parameters
- `shutdown()` and `awaitTermination()`
- `CompletableFuture`
- Stack, heap and GC Roots
- IoC and dependency injection
- `@Async`
- Spring Boot lazy initialization
- Starter dependencies
- Spring Cloud components
- Spring Cloud vs Kubernetes responsibilities

## Next 20 learning units

Follow this queue unless an interview or job description creates a more urgent requirement.

1. Spring Bean lifecycle
2. AOP proxy, JDK proxy and CGLIB
3. `@Transactional` mechanism and failure cases
4. Transaction propagation
5. Spring Boot auto-configuration
6. HashMap internals and resize
7. `equals()` and `hashCode()`
8. ThreadPoolExecutor execution flow
9. CompletableFuture timeout/error/partial success
10. Java Memory Model and happens-before
11. SQL indexes and execution plans
12. Isolation levels, MVCC and deadlocks
13. Redis cache problems and consistency
14. REST idempotency and error design
15. Retry, timeout and circuit breaker
16. Distributed transaction and Saga
17. JVM GC and production troubleshooting
18. Payment/API aggregation system design
19. OTT Pay project deep dive in English
20. Behavioural STAR mock

## Definition of “complete”

A learning unit can be checked off only after:

- Chinese closed-book explanation is correct;
- English answer is at least 60 seconds and technically correct;
- two follow-up questions are answered;
- one trade-off or failure mode is explained;
- code or a verified project example is supplied when appropriate.
