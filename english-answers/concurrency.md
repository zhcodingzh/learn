# Concurrency English Answers

These are reference structures. They must be practised without reading.

## Why is volatile not enough for count++?

`volatile` guarantees visibility, so one thread can observe the latest value written by another thread. However, `count++` is a read-modify-write operation and is not atomic. Two threads can read the same old value and overwrite each other's updates. For a counter, I would normally use `AtomicInteger`, `LongAdder`, or a lock depending on the consistency and contention requirements.

## synchronized vs ReadWriteLock

`synchronized` is usually my first choice for a simple critical section because it is easy to reason about and automatically releases the monitor. A `ReadWriteLock` separates shared reads from exclusive writes, so it may improve concurrency in a read-heavy workload. However, it adds overhead and complexity, and it is not guaranteed to be faster. I would choose it only when reads dominate, contention is meaningful and measurement supports the decision.

## What is StampedLock optimistic reading?

`StampedLock` supports an optimistic read that initially proceeds without acquiring a traditional read lock. After copying the values, the reader validates the stamp. If a writer modified the protected state, validation fails and the operation retries with a pessimistic read lock. This can reduce read-side contention, but the lock is not reentrant and is easier to misuse, so I would use it only for a proven read-heavy performance need.

## Why not coordinate three API calls with ConcurrentHashMap?

A `ConcurrentHashMap` provides thread-safe access to shared key-value data, but it is not a task-coordination abstraction. Checking whether the map contains three entries does not clearly represent failures, timeouts or duplicate keys. I may use the map to store results, but I would use `CompletableFuture.allOf()` or another coordination mechanism to determine when the operations have completed.

## CompletableFuture vs CountDownLatch

A `CountDownLatch` is useful when one thread needs to wait until a fixed number of operations finish. It coordinates completion but does not carry results, and exception handling is manual. `CompletableFuture` represents the result itself and supports composition, transformation and error handling. For aggregating several independent API responses in a Spring service, I would normally prefer `CompletableFuture`, together with a dedicated executor, timeouts and an explicit failure policy.

## Three external APIs

I would start the three independent calls concurrently using `CompletableFuture` and a dedicated executor suitable for blocking I/O. I would configure a timeout and exception policy for each call, then coordinate them with `allOf()` or typed combinations. After all required calls succeed, I would combine and validate the responses before saving the result. I would also decide whether a partial response is acceptable, because that business decision affects fallback and error handling.
