# Concurrency Question Bank

Answer without notes before reviewing the reference material.

## Foundation

1. What guarantees does `volatile` provide?
2. Why is `volatile int count` not enough for concurrent increments?
3. What memory guarantees does entering and leaving a synchronized block provide?
4. What is a race condition?
5. What is the difference between thread safety and atomicity?

## Locks

6. When would you choose `ReentrantLock` over `synchronized`?
7. How does `ReentrantReadWriteLock` allow concurrent reads?
8. Why can a read-write lock be slower than `synchronized`?
9. What is lock starvation?
10. How does a `StampedLock` optimistic read work?
11. Why must an optimistic read be validated?
12. What risks come from `StampedLock` not being reentrant?

## Coordination

13. What problem does `CountDownLatch` solve?
14. Why should `countDown()` normally be placed in `finally`?
15. Can a `CountDownLatch` be reused?
16. Why is `ConcurrentHashMap.size()` a weak completion signal?
17. When is a thread-safe collection still useful in an async workflow?

## CompletableFuture

18. What is the difference between `thenApply()` and `thenCompose()`?
19. What does `allOf()` return?
20. How do you retrieve typed results after `allOf()`?
21. How do you handle one failed API call?
22. How do you enforce timeouts?
23. Why can the common ForkJoinPool be risky for blocking I/O?
24. When would `thenCombine()` be clearer than `allOf()`?
25. How would you cancel or stop unnecessary downstream work?

## Senior scenarios

26. Three API calls are independent, but only two are required. How would you model partial success?
27. One API is slow and unreliable. Where should retry and circuit breaking be applied?
28. How would you prevent thread-pool exhaustion?
29. How would you monitor an asynchronous aggregation flow?
30. How would your design change if the operation must be completed exactly once?
