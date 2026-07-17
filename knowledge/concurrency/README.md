# Concurrency Notes

## 1. Three different problems

Before choosing a Java concurrency tool, identify the actual problem.

| Problem | Meaning | Common tools |
|---|---|---|
| Visibility | One thread must see another thread's latest write | `volatile`, locks, concurrent utilities |
| Mutual exclusion | A critical section must not be executed concurrently | `synchronized`, `Lock`, write lock |
| Task coordination | One task must wait for or combine other tasks | `CountDownLatch`, `CompletableFuture` |

A thread-safe collection solves safe concurrent data access. It does not automatically coordinate task completion.

## 2. volatile

`volatile` provides visibility and ordering guarantees for reads and writes to the variable.

It does not make compound operations such as `count++` atomic, and it does not provide mutual exclusion.

Use it for a state flag when:

- writes are simple;
- the new value does not depend on the old value;
- multiple fields do not need to change as one invariant.

## 3. synchronized

`synchronized` provides mutual exclusion and visibility around a monitor.

Good for:

- simple critical sections;
- protecting multiple related fields;
- code where advanced lock operations are unnecessary.

Limitations compared with `Lock` include less explicit control and no direct equivalent of timed `tryLock()`.

## 4. ReentrantReadWriteLock

It contains:

- a shared read lock;
- an exclusive write lock.

Multiple readers may hold the read lock together when there is no writer. A writer requires exclusive access.

It is useful when:

- reads greatly outnumber writes;
- protected operations are large enough for the extra lock overhead to be worthwhile;
- the data really requires consistent locking.

It is not automatically faster than `synchronized`. Measure contention and workload.

Always release a lock in `finally`.

## 5. StampedLock

`StampedLock` supports:

- write locking;
- pessimistic read locking;
- optimistic reading.

An optimistic read does not initially block a writer. The reader copies the values and then calls `validate(stamp)`. If validation fails, it retries under a real read lock.

Important limitations:

- it is not reentrant;
- it is easier to misuse;
- every successful lock acquisition must be matched with the correct stamp;
- it should be used only when read-heavy performance benefits justify the complexity.

## 6. ConcurrentHashMap

`ConcurrentHashMap` supports safe concurrent access to map data.

Use it when multiple threads need to share key-value data safely.

Do not use `map.size() == 3` as the primary completion mechanism for three asynchronous calls because:

- a map is a data container, not a task lifecycle abstraction;
- failure may prevent one entry from appearing;
- duplicate or replaced keys can make size misleading;
- polling size wastes resources;
- timeout and exception handling become unclear.

The map may store results, but completion should normally be coordinated separately.

## 7. CountDownLatch

A latch starts with a count. Each worker calls `countDown()`, usually in `finally`. The waiting thread calls `await()`.

It is appropriate when:

- a synchronous thread must wait for a known number of operations;
- the latch is used once;
- the code is based on threads or callback-style work rather than a composed result pipeline.

It does not directly carry return values and cannot be reset.

## 8. CompletableFuture

`CompletableFuture` represents a future result and supports asynchronous composition.

Key operations:

- `supplyAsync()`: start a task that returns a value;
- `thenApply()`: transform a completed value synchronously;
- `thenCompose()`: flatten a dependent asynchronous operation;
- `thenCombine()`: combine two results;
- `allOf()`: wait for several futures to finish;
- `exceptionally()` or `handle()`: process failure;
- `orTimeout()`: impose a timeout in supported Java versions.

For three independent API calls:

1. start three futures;
2. apply timeout and error policy to each;
3. use `allOf()` or combinations to coordinate completion;
4. collect the typed results;
5. validate business requirements;
6. persist or return the aggregate.

Use a dedicated executor for blocking I/O when appropriate. Do not blindly run blocking external API calls on the common ForkJoinPool.

## 9. CountDownLatch vs CompletableFuture

| Question | CountDownLatch | CompletableFuture |
|---|---|---|
| Main purpose | Wait for a count to reach zero | Compose asynchronous results |
| Carries results | No | Yes |
| Error composition | Manual | Built-in stages |
| Reusable | No | Each future is one computation |
| Best fit | Thread coordination | Async result pipelines |

For a modern service aggregating three API results, `CompletableFuture` is usually the clearer abstraction. A latch is reasonable when integrating older callback or thread-based code.

## Interview decision rule

Ask:

1. Am I protecting shared mutable state?
2. Am I only making a value visible?
3. Am I coordinating completion?
4. Do I need returned values?
5. What is the timeout and failure policy?
6. Is the work CPU-bound or blocking I/O?
