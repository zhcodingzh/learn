# Weekly Plan — Week 1

**Period:** July 16–22, 2026  
**Primary goal:** distinguish data safety, mutual exclusion and task coordination.

## Topics and initial estimated mastery

| Topic | Initial level | Target |
|---|---:|---:|
| volatile | 2 | 4 |
| synchronized | 3 | 4 |
| ReentrantReadWriteLock | 2 | 4 |
| StampedLock | 2 | 3 |
| ConcurrentHashMap | 2 | 4 |
| CountDownLatch | 2 | 4 |
| CompletableFuture | 2 | 4 |
| ThreadPoolExecutor | 1 | 3 |

These levels are provisional until verified by closed-book answers.

## Daily plan

### July 16

- Confirm the difference between visibility and mutual exclusion.
- Review `volatile`, `synchronized` and `ReadWriteLock`.
- Give a 60-second English answer.

### July 17

- Closed-book D1 review.
- Compare `ConcurrentHashMap` with coordination utilities.
- Explain why map size should not be used as the completion signal.

### July 18

- Learn `CompletableFuture` composition.
- Compare `thenApply`, `thenCompose` and `allOf`.
- Write or explain a three-API aggregation example.

### July 19

- D3 English review.
- Add timeout and exception handling.
- Compare `CompletableFuture.allOf()` and `CountDownLatch`.

### July 20

- Review `StampedLock` optimistic reading and validation.
- Compare it with `ReadWriteLock`.

### July 21

- Learn executor sizing and common thread-pool risks.
- Explain why the common pool may be inappropriate for blocking API calls.

### July 22

- Mixed concurrency mock interview.
- Update mastery levels and mistake log.
- Schedule D7 and D14 reviews.

## Completion criteria

Week 1 is complete only when I can:

- Explain each major topic without notes.
- Give a 60–90 second English answer.
- Answer at least two follow-up questions.
- Select the correct mechanism for a practical scenario.
