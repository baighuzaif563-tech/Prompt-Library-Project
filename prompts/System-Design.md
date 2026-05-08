# 🏗️ System Design Prompt Library — Developer Edition

> A structured collection of **high-quality AI prompts** for System Design  
> Built for **senior engineer interviews, architecture thinking, and scalable system building** 🚀

<br>

## 📋 Table of Contents

- [How to Use](#-how-to-use)
- [Prompt Quality Guide](#-prompt-quality-guide)
- [1. System Design Fundamentals](#-1-system-design-fundamentals)
- [2. Scalability & Load Balancing](#-2-scalability--load-balancing)
- [3. Databases & Storage](#-3-databases--storage)
- [4. Caching](#-4-caching)
- [5. Message Queues & Event-Driven Design](#-5-message-queues--event-driven-design)
- [6. API Design](#-6-api-design)
- [7. Microservices Architecture](#-7-microservices-architecture)
- [8. Distributed Systems](#-8-distributed-systems)
- [9. Real-World System Designs](#-9-real-world-system-designs)
- [10. System Design Interview Practice](#-10-system-design-interview-practice)
- [11. Master System Design Prompt](#-11-master-system-design-prompt)
- [Final Goal](#-final-goal)

---

## 🎯 How to Use

```
1. Pick a topic from the list
2. Copy the ✅ Good Prompt
3. Paste into your AI tool (Claude, ChatGPT, etc.)
4. Get structured architecture explanation + diagrams
5. Practice whiteboarding the design yourself
```

---

## ⚡ Prompt Quality Guide

| Badge | Meaning |
|-------|---------|
| ✅ **Good Prompt** | Structured, deep explanation, interview-ready output |
| ❌ **Bad Prompt** | Vague, short, produces low-quality response |

> **Rule of Thumb:** Always define scale requirements (users, QPS, data size) in your prompt.

---

## 🧱 1. System Design Fundamentals

### How to Approach System Design

| | Prompt |
|--|--------|
| ✅ | `Teach me a step-by-step framework for tackling any system design interview — covering requirement gathering, capacity estimation, high-level design, component deep-dives, bottleneck identification, and trade-off discussion with a worked example.` |
| ❌ | `How to do system design?` |

<details>
<summary>📌 Expected Output</summary>

- 5-step framework (Clarify → Estimate → Design → Deep Dive → Trade-offs)
- Functional vs non-functional requirements
- Back-of-the-envelope estimation techniques
- Common components to always consider
- Time management during interviews

</details>

---

### Capacity Estimation

| | Prompt |
|--|--------|
| ✅ | `Teach me back-of-the-envelope estimation for system design — cover QPS calculation, storage estimation, bandwidth calculation, memory sizing, and work through a Twitter-scale example step by step.` |
| ❌ | `How to estimate in system design?` |

<details>
<summary>📌 Expected Output</summary>

- QPS = DAU × actions/day ÷ 86,400
- Read/write ratio estimation
- Storage calculation (bytes × records × time)
- Bandwidth from data size × QPS
- Memory cache sizing (20% of daily data rule)

</details>

---

## ⚖️ 2. Scalability & Load Balancing

### Horizontal vs Vertical Scaling

| | Prompt |
|--|--------|
| ✅ | `Explain horizontal vs vertical scaling in system design — compare cost, limits, failure modes, and when to use each. Include real-world examples and how companies like Netflix and Amazon scale their systems.` |
| ❌ | `Explain scaling.` |

<details>
<summary>📌 Expected Output</summary>

- Vertical scaling ceiling
- Horizontal scaling with stateless services
- Database scaling challenges
- Auto-scaling groups (AWS ASG)
- When vertical scaling is correct choice

</details>

---

### Load Balancers

| | Prompt |
|--|--------|
| ✅ | `Explain load balancers in system design — L4 vs L7 load balancers, algorithms (round robin, least connections, consistent hashing, IP hash), health checks, session persistence, and how to avoid single points of failure.` |
| ❌ | `What is a load balancer?` |

<details>
<summary>📌 Expected Output</summary>

- L4 (TCP/UDP) vs L7 (HTTP) differences
- Round robin vs weighted round robin
- Consistent hashing for stateful services
- Active-passive vs active-active setup
- Load balancer as potential SPOF

</details>

---

### CDN & Edge Computing

| | Prompt |
|--|--------|
| ✅ | `Explain CDNs in system design — how they work, push vs pull CDN, cache invalidation strategies, edge computing, when to use a CDN, and how a CDN reduces load on origin servers with a design example.` |
| ❌ | `What is a CDN?` |

<details>
<summary>📌 Expected Output</summary>

- PoP (Points of Presence) network
- Pull CDN vs push CDN tradeoffs
- Cache-Control headers and TTL
- CDN for static and dynamic content
- When NOT to use a CDN

</details>

---

## 🗄️ 3. Databases & Storage

### SQL vs NoSQL

| | Prompt |
|--|--------|
| ✅ | `Compare SQL and NoSQL databases for system design — cover ACID vs BASE, schema flexibility, scaling patterns, consistency models, and give concrete examples of when to choose PostgreSQL, MongoDB, Cassandra, or DynamoDB.` |
| ❌ | `SQL vs NoSQL.` |

<details>
<summary>📌 Expected Output</summary>

- ACID vs BASE tradeoffs
- Vertical vs horizontal scaling patterns
- When consistency matters vs availability
- NoSQL types: document, key-value, column, graph
- Polyglot persistence pattern

</details>

---

### Database Replication & Sharding

| | Prompt |
|--|--------|
| ✅ | `Explain database replication and sharding in system design — master-slave vs master-master replication, read replicas, horizontal sharding strategies (range, hash, directory), resharding challenges, and hotspot prevention.` |
| ❌ | `What is database sharding?` |

<details>
<summary>📌 Expected Output</summary>

- Replication lag and eventual consistency
- Read replicas for read-heavy workloads
- Hash sharding vs range sharding
- Consistent hashing for shard assignment
- Cross-shard query problems

</details>

---

### Storage Systems

| | Prompt |
|--|--------|
| ✅ | `Compare storage options in system design — block storage, object storage, file storage, in-memory storage — with AWS equivalents (EBS, S3, EFS, ElastiCache), use cases, and cost/performance tradeoffs.` |
| ❌ | `Types of storage in system design.` |

<details>
<summary>📌 Expected Output</summary>

- Block vs object vs file storage
- S3 for media and large objects
- When to use NFS/distributed file system
- In-memory for session and cache
- Data durability and replication

</details>

---

## ⚡ 4. Caching

### Caching Strategies

| | Prompt |
|--|--------|
| ✅ | `Explain caching in system design — cache-aside, read-through, write-through, write-back, write-around strategies — with Redis examples, eviction policies (LRU, LFU, TTL), cache stampede prevention, and when each strategy is appropriate.` |
| ❌ | `Explain caching.` |

<details>
<summary>📌 Expected Output</summary>

- Cache-aside (lazy loading) pattern
- Write-through vs write-back consistency
- LRU vs LFU eviction comparison
- Cache stampede and dog-pile effect
- Consistent hashing for distributed cache

</details>

---

### Redis vs Memcached

| | Prompt |
|--|--------|
| ✅ | `Compare Redis and Memcached for system design — data structures, persistence, replication, clustering, pub/sub, Lua scripting, and give concrete use cases where each is the right choice.` |
| ❌ | `Redis vs Memcached.` |

<details>
<summary>📌 Expected Output</summary>

- Redis data structures (strings, hashes, lists, sets, sorted sets)
- Redis persistence (RDB snapshots, AOF logs)
- Memcached: simple, multi-threaded, pure cache
- Redis clustering and sentinel
- Use cases: leaderboard, rate limiting, session store

</details>

---

## 📨 5. Message Queues & Event-Driven Design

### Message Queues

| | Prompt |
|--|--------|
| ✅ | `Explain message queues in system design — why they're used, producer-consumer pattern, Kafka vs RabbitMQ vs SQS comparison, at-least-once vs exactly-once delivery, consumer groups, and dead letter queues with real use cases.` |
| ❌ | `What is a message queue?` |

<details>
<summary>📌 Expected Output</summary>

- Decoupling producers and consumers
- Kafka: log-based, high throughput, replay
- RabbitMQ: traditional queue, routing, push
- At-most-once / at-least-once / exactly-once
- Dead letter queue for failed messages

</details>

---

### Event-Driven Architecture

| | Prompt |
|--|--------|
| ✅ | `Explain event-driven architecture — events vs commands vs queries, event sourcing, CQRS pattern, saga pattern for distributed transactions, and how Uber and Airbnb use event-driven design at scale.` |
| ❌ | `What is event-driven architecture?` |

<details>
<summary>📌 Expected Output</summary>

- Events vs commands distinction
- Event sourcing and event store
- CQRS: separate read and write models
- Saga: choreography vs orchestration
- Eventual consistency in event systems

</details>

---

## 🔌 6. API Design

### REST vs GraphQL vs gRPC

| | Prompt |
|--|--------|
| ✅ | `Compare REST, GraphQL, and gRPC for API design — cover protocol, performance, schema, use cases, over-fetching/under-fetching, streaming support, and when to choose each in system design interviews.` |
| ❌ | `REST vs GraphQL vs gRPC.` |

<details>
<summary>📌 Expected Output</summary>

- REST: stateless, HTTP verbs, wide support
- GraphQL: flexible queries, single endpoint
- gRPC: binary protocol, streaming, microservices
- When each is appropriate
- API gateway and BFF pattern

</details>

---

### API Rate Limiting

| | Prompt |
|--|--------|
| ✅ | `Explain API rate limiting in system design — token bucket, leaky bucket, fixed window, sliding window log, sliding window counter algorithms — with Redis implementation, distributed rate limiting, and where to place the rate limiter.` |
| ❌ | `How to implement rate limiting?` |

<details>
<summary>📌 Expected Output</summary>

- Token bucket vs leaky bucket
- Fixed vs sliding window tradeoffs
- Redis + Lua script for atomic rate limiting
- Distributed rate limiting across nodes
- Rate limit headers (X-RateLimit-*)

</details>

---

## 🔧 7. Microservices Architecture

### Microservices vs Monolith

| | Prompt |
|--|--------|
| ✅ | `Compare monolithic vs microservices architecture — deployment, scaling, team structure, failure isolation, data management, service discovery, and when to migrate from monolith to microservices with a real migration strategy.` |
| ❌ | `Microservices vs monolith.` |

<details>
<summary>📌 Expected Output</summary>

- Monolith: simple, consistent, hard to scale independently
- Microservices: independent deploy, bounded context
- Conway's Law and team structure
- Strangler fig migration pattern
- When microservices are wrong choice

</details>

---

### Service Discovery & Communication

| | Prompt |
|--|--------|
| ✅ | `Explain service discovery and inter-service communication in microservices — client-side vs server-side discovery, service registry (Consul, Eureka), synchronous (REST, gRPC) vs asynchronous (Kafka, RabbitMQ) communication, and circuit breaker pattern.` |
| ❌ | `How do microservices communicate?` |

<details>
<summary>📌 Expected Output</summary>

- Service registry pattern
- Health checks and deregistration
- Synchronous vs async tradeoffs
- Circuit breaker (Hystrix/Resilience4j)
- Bulkhead and retry patterns

</details>

---

## 🌐 8. Distributed Systems

### CAP Theorem

| | Prompt |
|--|--------|
| ✅ | `Explain the CAP theorem for distributed systems — Consistency, Availability, Partition tolerance — why you can only pick two, CP vs AP system examples, and how real systems like Cassandra, DynamoDB, and ZooKeeper make this tradeoff.` |
| ❌ | `What is CAP theorem?` |

<details>
<summary>📌 Expected Output</summary>

- Network partition as unavoidable
- CP systems: strong consistency (ZooKeeper)
- AP systems: high availability (Cassandra)
- PACELC as extension to CAP
- Tunable consistency in Cassandra

</details>

---

### Consistent Hashing

| | Prompt |
|--|--------|
| ✅ | `Explain consistent hashing in distributed systems — the ring concept, virtual nodes, how it minimizes resharding, and real-world use in distributed caches (Redis Cluster), load balancers, and databases like Cassandra and DynamoDB.` |
| ❌ | `What is consistent hashing?` |

<details>
<summary>📌 Expected Output</summary>

- Hash ring visualization
- Problem with naive modulo hashing
- Virtual nodes for even distribution
- Hotspot prevention
- Cassandra partition key design

</details>

---

## 💡 9. Real-World System Designs

### Design URL Shortener

| | Prompt |
|--|--------|
| ✅ | `Design a URL shortener system like bit.ly — define requirements (scale: 100M URLs, 10B redirects/month), design the schema, API, short code generation (base62), database choice, caching layer, and how to handle analytics and expiry.` |
| ❌ | `Design a URL shortener.` |

<details>
<summary>📌 Expected Output</summary>

- Functional requirements (shorten, redirect, analytics)
- 7-character base62 encoding
- SQL for metadata, Redis for redirect cache
- 301 vs 302 redirect choice
- Rate limiting per user

</details>

---

### Design a Chat System

| | Prompt |
|--|--------|
| ✅ | `Design a real-time chat system like WhatsApp — cover 1-on-1 and group messaging, WebSocket connections, message storage, delivery receipts (sent/delivered/read), online presence, push notifications, and how to scale to 1 billion users.` |
| ❌ | `Design a chat app.` |

<details>
<summary>📌 Expected Output</summary>

- WebSocket for real-time bidirectional
- Connection server vs chat server
- Message persistence and ordering
- Delivery receipt state machine
- Group chat fanout strategies

</details>

---

### Design a Video Streaming Platform

| | Prompt |
|--|--------|
| ✅ | `Design a video streaming platform like YouTube — cover video upload pipeline, transcoding to multiple resolutions, CDN delivery, adaptive bitrate streaming (HLS/DASH), search/recommendation, storage, and how to handle 500 hours of video uploaded per minute.` |
| ❌ | `Design YouTube.` |

<details>
<summary>📌 Expected Output</summary>

- Upload pipeline (blob storage → message queue → transcoder)
- FFmpeg transcoding job workers
- HLS chunking and manifest files
- CDN edge caching strategy
- View count with eventual consistency

</details>

---

### Design a Ride-Sharing App

| | Prompt |
|--|--------|
| ✅ | `Design a ride-sharing system like Uber — cover location updates, driver-rider matching, geospatial indexing (QuadTree/S2), surge pricing, trip state machine, payment processing, and how to handle 10M concurrent users across cities.` |
| ❌ | `Design Uber.` |

<details>
<summary>📌 Expected Output</summary>

- Geospatial indexing with QuadTree
- Driver location update frequency
- Matching algorithm and dispatch
- Trip state machine (requested → accepted → in-progress → completed)
- ETA calculation service

</details>

---

## 🧪 10. System Design Interview Practice

### Mock System Design Interview

| | Prompt |
|--|--------|
| ✅ | `Act as a system design interviewer at Google/Meta. Give me a system design problem, ask clarifying questions when I try to skip steps, evaluate my design for scalability and correctness, and give structured feedback at the end.` |
| ❌ | `Give system design questions.` |

<details>
<summary>📌 Expected Output</summary>

- Interactive interview format
- Probing questions on scale and edge cases
- Hints when stuck without giving away answer
- Evaluation on completeness and trade-offs
- Structured feedback and improvement areas

</details>

---

## 🚀 11. Master System Design Prompt

### The Ultimate All-in-One Prompt

```
Teach me System Design from beginner to advanced — cover:
scalability fundamentals, load balancing, databases (SQL/NoSQL, sharding, replication),
caching strategies, message queues, API design, microservices, distributed systems
(CAP theorem, consistent hashing), and walk me through designing 5 real systems:
URL shortener, chat app, video streaming, ride-sharing, and news feed.
Include component diagrams, trade-off discussions, and capacity estimates for each.
```

> ❌ **Bad version:** `Teach me system design.`

<details>
<summary>📌 Expected Output</summary>

- Full structured roadmap
- Each component explained with diagrams
- 5 complete system designs with trade-offs
- Interview framework and time management
- Common mistakes to avoid

</details>

---

## 🏁 Final Goal

This prompt library helps you:

| Goal | What it does |
|------|-------------|
| 💼 Senior Interview Ready | Crack L5/L6 system design rounds at FAANG |
| 🏗️ Architecture Thinking | Design scalable, reliable systems from scratch |
| ⚖️ Trade-off Analysis | Justify every design decision with clear reasoning |
| 📐 Estimation Skills | Do back-of-envelope calculations confidently |
| 🔍 Deep Dives | Go beyond surface-level into real internals |

---

## 🔥 Pro Tips

> **Interview Preparation Formula:**
> ```
> 1 system design/week (deep study) + 1 mock interview/week = FAANG-ready in 2-3 months
> ```

- **Always clarify scale first** — the right answer at 1K users is wrong at 100M users
- **Draw the diagram before writing anything** — start with boxes and arrows
- **Discuss trade-offs proactively** — interviewers want to see you know the downsides
- **Know the numbers**: 1 server = ~10K QPS, Redis = ~100K QPS, Kafka = ~1M msg/sec
- **Study real architectures**: Netflix tech blog, AWS re:Invent, Uber engineering blog

---

## 📚 Recommended Resources

| Resource | What to Learn |
|----------|--------------|
| [Designing Data-Intensive Applications](https://dataintensive.net/) | Deep distributed systems theory |
| [System Design Primer (GitHub)](https://github.com/donnemartin/system-design-primer) | Comprehensive visual guide |
| [ByteByteGo](https://bytebytego.com/) | Visual system design explanations |
| [AWS Architecture Blog](https://aws.amazon.com/blogs/architecture/) | Real-world architectures |
| [High Scalability Blog](http://highscalability.com/) | How real companies scaled |

---

## 🤝 Contributing

Have a better prompt? Found a pattern that works well?

1. Fork this repo
2. Add your prompt in the relevant section
3. Follow the `✅ Good Prompt / ❌ Bad Prompt / 📌 Expected Output` format
4. Open a Pull Request

---

## ⭐ Star This Repo

If this helped you, please give it a ⭐ — it helps others find it too!

---

<p align="center">Made with ❤️ for every developer on their System Design journey</p>
