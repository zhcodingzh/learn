# Mistake Log

This file records recurring reasoning errors, not every small wording issue.

| Date | Topic | Initial misunderstanding | Correct model | Retest |
|---|---|---|---|---|
| 2026-07-16 | volatile | Visibility may be confused with mutual exclusion | volatile provides visibility/order, not a critical section | D1 |
| 2026-07-16 | ConcurrentHashMap | Map size may be treated as task completion | Data safety and task coordination are different concerns | D1 |
| 2026-07-16 | CountDownLatch | Latch and result storage may be treated as alternatives | Latch coordinates completion; another structure carries results | D3 |
| 2026-07-16 | CompletableFuture | `allOf()`, `thenApply()` and callbacks need clearer separation | Use stages according to dependency and composition needs | D3 |
| 2026-07-16 | ReadWriteLock | Read concurrency may be described without its conditions | Readers share only when no incompatible writer owns the lock | D3 |

## Entry template

- Date:
- Question:
- My answer:
- Exact technical error:
- Correct mental model:
- English correction:
- Follow-up question:
- Next review:
