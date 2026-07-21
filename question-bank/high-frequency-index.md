# High-Frequency Senior Java Question Index

Use this bank for voice review and mock interviews. Ask one question at a time.

## Resume and project

1. Tell me about yourself.
2. Walk me through the architecture of your most recent system.
3. What was your most technically difficult contribution?
4. Describe a production incident you diagnosed.
5. How did you measure whether your fix worked?
6. What trade-off did you make and why?
7. What would you redesign today?
8. How did you handle security or code-quality risks?
9. How did you work across teams or services?
10. What made your responsibility Senior-level?

## Java core and collections

11. Why is String immutable?
12. What is the difference between `==` and `equals()`?
13. What is the contract between `equals()` and `hashCode()`?
14. How does HashMap work internally?
15. What happens during a HashMap collision?
16. When does a bucket become a red-black tree?
17. How does HashMap resize, and why is resize unsafe concurrently?
18. ArrayList vs LinkedList: how do you choose?
19. HashMap vs ConcurrentHashMap?
20. Checked vs unchecked exceptions?
21. `throw` vs `throws`?
22. `map()` vs `flatMap()`?
23. How does Java generic type erasure work?
24. When should Optional not be used?
25. Explain immutable-object design.

## Concurrency

26. What guarantees does `volatile` provide?
27. Why is `count++` not made safe by `volatile`?
28. What does happens-before mean?
29. How does `synchronized` work?
30. `synchronized` vs `ReentrantLock`?
31. When would you use `ReadWriteLock`?
32. How does `StampedLock` optimistic reading work?
33. What is CAS and what is the ABA problem?
34. `AtomicLong` vs `LongAdder`?
35. How does ConcurrentHashMap provide concurrency?
36. `compute()` vs `computeIfAbsent()`?
37. What causes a deadlock and how do you diagnose it?
38. Explain all important ThreadPoolExecutor parameters.
39. What happens when a thread-pool task is submitted?
40. How do you choose a thread-pool size?
41. What do `shutdown()`, `shutdownNow()` and `awaitTermination()` do?
42. `CountDownLatch` vs `CyclicBarrier`?
43. `thenApply()` vs `thenCompose()`?
44. `thenCombine()` vs `allOf()`?
45. How would you call three external APIs concurrently?
46. How would you handle timeout, failure and partial success?
47. Why can blocking I/O on the common ForkJoinPool be dangerous?

## JVM and GC

48. Explain JVM runtime memory areas.
49. What is stored in a stack frame?
50. How does the JVM determine whether an object is alive?
51. What are common GC Roots?
52. Minor GC vs full GC?
53. What is stop-the-world?
54. How does G1 work at a high level?
55. What causes an OutOfMemoryError?
56. Memory leak vs OOM?
57. Explain class loading and parent delegation.
58. How would you investigate high CPU?
59. How would you investigate increasing heap usage?
60. What information do thread dumps and heap dumps provide?

## Spring and Spring Boot

61. What are IoC and dependency injection?
62. Why prefer constructor injection?
63. Explain the Spring Bean lifecycle.
64. How does Spring handle circular dependencies?
65. How does Spring AOP work?
66. JDK dynamic proxy vs CGLIB?
67. Why can self-invocation break `@Transactional` or `@Async`?
68. Explain the Spring MVC request lifecycle.
69. Filter vs Interceptor vs AOP?
70. How does Spring Boot auto-configuration work?
71. What is a starter dependency?
72. What do conditional annotations do?
73. What are the benefits and risks of lazy initialization?
74. How does `@Transactional` work?
75. REQUIRED vs REQUIRES_NEW?
76. When does a transaction fail to roll back?
77. What happens when a transactional method calls another method in the same class?
78. How do you design global exception handling?
79. How does Spring Security authentication work?
80. Explain a JWT request flow.
81. Unit test vs Spring integration test?
82. When would you use Testcontainers?

## SQL and persistence

83. How does a B+tree index work?
84. What is a composite index?
85. Explain the leftmost-prefix rule.
86. What is a covering index?
87. Why might a query not use an index?
88. How do you diagnose a slow query?
89. Explain ACID.
90. Explain database isolation levels and anomalies.
91. How does MVCC work?
92. Optimistic vs pessimistic locking?
93. How do database deadlocks occur?
94. What is the N+1 query problem?
95. Lazy vs eager loading?
96. How do you paginate a very large table?
97. What problems can replication lag cause?
98. How do you choose a sharding key?
99. How do you size a database connection pool?

## Redis and messaging

100. What Redis data structures have you used?
101. Explain cache-aside.
102. Cache penetration vs breakdown vs avalanche?
103. How do you keep cache and database consistent?
104. How do you handle hot keys?
105. RDB vs AOF?
106. How does a distributed lock work safely?
107. How do you implement idempotency with Redis?
108. Why use a message queue?
109. At-most-once vs at-least-once delivery?
110. How do you handle duplicate consumption?
111. How do you preserve message ordering?
112. What is a dead-letter queue?
113. Explain the outbox pattern.
114. How do you handle consumer lag?

## REST, microservices and distributed systems

115. What makes an API RESTful?
116. Which HTTP methods are idempotent?
117. How do you design consistent API errors?
118. How do you version an API?
119. What belongs in an API Gateway?
120. Service discovery: Spring Cloud vs Kubernetes?
121. Why must every remote call have a timeout?
122. When is retry dangerous?
123. How does a circuit breaker work?
124. What is a bulkhead?
125. How do you implement rate limiting?
126. What is an idempotency key?
127. What does eventual consistency mean?
128. What is the Saga pattern?
129. Explain CAP using a practical example.
130. How do you trace one request across services?
131. How do you handle partial failure?
132. How do you make a backward-compatible change?

## Kubernetes, delivery and observability

133. Docker image vs container?
134. Pod vs Deployment vs Service?
135. Readiness vs liveness?
136. ConfigMap vs Secret?
137. Requests vs limits?
138. How does rolling deployment work?
139. How would you roll back a bad release?
140. Kubernetes service discovery vs Eureka?
141. Logs vs metrics vs traces?
142. What would you monitor for an external-API integration?
143. How do you avoid noisy or useless alerts?
144. Blue-green vs canary deployment?

## System design

145. How do you clarify requirements before designing?
146. Design an idempotent payment API.
147. Design a service that aggregates three external APIs.
148. Design an order-processing system.
149. Design a notification system.
150. Design a rate limiter.
151. Design a risk-rule management platform.
152. Where would you cache, and how would you invalidate it?
153. How would your design survive a dependency outage?
154. What would you measure in production?
155. How would you scale the database?
156. How would you protect sensitive data?

## Behavioural

157. Tell me about a difficult production issue.
158. Tell me about a disagreement.
159. Tell me about a failure or missed deadline.
160. Tell me about mentoring or code review.
161. Tell me about ambiguous requirements.
162. Tell me about improving performance.
163. Tell me about improving reliability.
164. How do you prioritize competing work?
165. Why are you looking for a new role?
166. Why this company?
167. What is one development area you are working on?
168. How do you keep technical knowledge current?
