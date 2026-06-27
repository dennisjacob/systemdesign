# Master System Design & Architecture Curriculum

A comprehensive, hierarchical system design and architecture curriculum designed for principal-level engineering interviews and production-scale system design.

[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)

> **Acknowledge**: This work is derived from original material by Dennis Jacob. When copying or adapting, please retain attribution to the original author.

---

## Table of Contents

| Section | Title | Documents |
|---------|-------|-----------|
| [1](#section-1-architectural-foundations) | Architectural Foundations | 3 modules |
| [2](#section-2-networking) | Networking | 3 modules |
| [3](#section-3-ha-traffic-engineering) | High-Availability Traffic Engineering | 4 modules |
| [4](#section-4-data-modeling) | Data Modeling | 5 modules |
| [5](#section-5-memory-caching) | Memory & Caching | 4 modules |
| [6](#section-6-distributed-coordination) | Distributed Coordination | 3 modules |
| [7](#section-7-integration-architecture) | Integration Architecture | 3 modules |
| [8](#section-8-software-architecture) | Software Architecture | 8 modules |
| [9](#section-9-platform-devops) | Platform & DevOps | 2 modules |
| [10](#section-10-production-engineering) | Production Engineering | 3 modules |
| [11](#section-11-ai-systems) | AI Systems | 10 modules |
| [12](#section-12-multi-region) | Multi-Region Architecture | 3 modules |
| [13](#section-13-design-tradeoffs) | Design Trade-offs | 1 module |
| [14](#section-14-case-studies) | Case Studies | 8 modules |

---

## Section 1: Architectural Foundations

**Scale Engineering Primitives & Core Hardware Primitives**

Understanding the fundamental trade-offs between performance and scalability is essential for every architectural decision.

| Module | Title | Description |
|--------|-------|-------------|
| [1.1](1-Architectural-Foundations/1.1-Scale-Engineering-Primitives-Enhanced-v1.0.06-06.md) | Scale Engineering Primitives | Performance vs. scalability, latency vs. throughput, concurrency models, capacity estimation |
| [1.2](1-Architectural-Foundations/1.2-Computational-OS-Primitives-Enhanced-v1.0.06-06.md) | Computational & OS Primitives | Processes vs. threads, memory management, I/O patterns, Linux diagnostics |
| [1.3](1-Architectural-Foundations/1.3-Physical-Hardware-Boundaries-Enhanced-v1.0.06-06.md) | Physical Hardware Boundaries | Memory hierarchy, storage tiers, network latency, NUMA effects |

---

## Section 2: Networking

**Advanced Networking Models, Traffic Topology & Edge Infrastructure**

Building the foundation for reliable, secure, and performant network communication.

| Module | Title | Description |
|--------|-------|-------------|
| [2.1](2-Networking/2.1-Networking-Models-v1.0.06-06.md) | Networking Models & Protocols | OSI model, TCP/IP stack, HTTP/3, QUIC, port configurations |
| [2.2](2-Networking/2.2-Ingress-Topology-v1.0.06-06.md) | Ingress Topology & Proxies | Load balancing strategies, reverse proxies, service mesh patterns |
| [2.3](2-Networking/2.3-Encryption-TLS-v1.0.06-06.md) | Encryption & TLS | TLS handshakes, certificate management, mutual TLS, secure transport |

---

## Section 3: HA Traffic Engineering

**High-Availability Traffic Engineering & Edge Caching**

Multi-region, high-availability gateway topologies and content delivery patterns.

| Module | Title | Description |
|--------|-------|-------------|
| [3.1](3-HA-Traffic-Engineering/3.1-HA-Gateway-Topologies-v1.0.06-07.md) | HA Gateway Topologies | Active-active, active-passive, geographic routing, failover strategies |
| [3.2](3-HA-Traffic-Engineering/3.2-CDNs-Distributed-Asset-Delivery-v1.0.06-07.md) | CDNs & Asset Delivery | CDN architecture, cache invalidation, edge computing |
| [3.3](3-HA-Traffic-Engineering/3.3-Video-Processing-Media-Delivery-v1.0.06-07.md) | Video Processing & Media Delivery | Transcoding pipelines, adaptive streaming, content distribution |
| [3.4](3-HA-Traffic-Engineering/3.4-Distributed-File-Systems-v1.0.06-07.md) | Distributed File Systems | Object storage, block storage, consistency models, replication |

---

## Section 4: Data Modeling

**Database Taxonomy, Engine Internals & Distributed Storage**

Comprehensive data architecture from relational to modern lakehouse patterns.

| Module | Title | Description |
|--------|-------|-------------|
| [4.1](4-Data-Modeling/4.1-Database-Taxonomy-v1.0.06-07.md) | Database Taxonomy | SQL vs NoSQL selection, relational databases, key-value stores, document stores |
| [4.2](4-Data-Modeling/4.2-Relational-Tuning-v1.0.06-07.md) | Relational Tuning & Scaling | Indexing strategies, query optimization, sharding approaches |
| [4.3](4-Data-Modeling/4.3-Storage-Engine-Concurrency-v1.0.06-07.md) | Storage Engine & Concurrency | B-trees, LSM trees, MVCC, lock-free structures |
| [4.4](4-Data-Modeling/4.4-Data-Warehouses-Lakehouses-v1.0.06-07.md) | Data Warehouses & Lakehouses | Star schemas, columnar storage, Delta Lake, Iceberg |
| [4.5](4-Data-Modeling/4.5-Time-Series-Spatial-Indexing-v1.0.06-07.md) | Time Series & Spatial Indexing | TimescaleDB, InfluxDB, geospatial queries, vector search |

---

## Section 5: Memory & Caching

**Memory Management, Caching Strategies & WAL Systems**

Multi-tier caching architectures and write-ahead log optimization.

| Module | Title | Description |
|--------|-------|-------------|
| [5.1](5-Memory-Caching/5.1-Cache-Architectures-v1.0.06-07.md) | Cache Tier Architectures | Cache-aside, read-through, write-through, write-behind patterns |
| [5.2](5-Memory-Caching/5.2-Cache-Strategies-v1.0.06-07.md) | Cache Strategies & Failures | TTL management, cache warming, thundering herd prevention |
| [5.3](5-Memory-Caching/5.3-Probabilistic-Data-Structures-v1.0.06-07.md) | Probabilistic Data Structures | Bloom filters, HyperLogLog, Count-Min Sketch |
| [5.4](5-Memory-Caching/5.4-WAL-Platform-Speeds-v1.0.06-07.md) | WAL Primitives & Processing | Write-ahead logging, database durability, platform performance |

---

## Section 6: Distributed Coordination

**Consistency Models, Consensus & Transaction Orchestration**

Distributed systems correctness and coordination patterns.

| Module | Title | Description |
|--------|-------|-------------|
| [6.1](6-Distributed-Coordination/6.1-Consistency-Models-v1.0.06-07.md) | Consistency Models | Strong, eventual, causal consistency; CAP theorem, PACELC |
| [6.2](6-Distributed-Coordination/6.2-Consensus-Time-Orchestration-v1.0.06-07.md) | Consensus & Orchestration | Raft, Paxos, leader election, distributed locking |
| [6.3](6-Distributed-Coordination/6.3-Distributed-Transactions-v1.0.06-07.md) | Distributed Transactions | Two-phase commit, saga pattern, idempotency |

---

## Section 7: Integration Architecture

**Modern Integration, Event Streams & API Lifecycles**

Enterprise integration patterns and asynchronous messaging.

| Module | Title | Description |
|--------|-------|-------------|
| [7.1](7-Integration-Architecture/7.1-Enterprise-Integration-v1.0.06-07.md) | Enterprise Integration | ESB patterns, iPaaS, API-led connectivity |
| [7.2](7-Integration-Architecture/7.2-Async-Messaging-v1.0.06-07.md) | Async Messaging & Events | Kafka, RabbitMQ, event sourcing, CQRS |
| [7.3](7-Integration-Architecture/7.3-API-Lifecycle-Telemetry-v1.0.06-07.md) | API Lifecycle & Telemetry | API gateways, versioning strategies, observability |

---

## Section 8: Software Architecture

**Domain Modeling, Design Patterns & Low-Level Design**

Architectural patterns and design principles for maintainable systems.

| Module | Title | Description |
|--------|-------|-------------|
| [8.1](8-Software-Architecture/8.1-Domain-Driven-Design-v1.0.06-07.md) | Domain-Driven Design | Bounded contexts, aggregates, value objects, domain events |
| [8.2](8-Software-Architecture/8.2-Clean-Hexagonal-Architecture-v1.0.06-07.md) | Clean & Hexagonal Architecture | Ports & adapters, dependency inversion, separation of concerns |
| [8.3](8-Software-Architecture/8.3-Object-Oriented-LLD-v1.0.06-07.md) | Object-Oriented LLD | SOLID principles, design patterns, class diagrams |
| [8.4](8-Software-Architecture/8.4-Serverless-Architecture-v1.0.06-07.md) | Serverless Architecture | Function-as-a-Service, cold starts, vendor lock-in |
| [8.5](8-Software-Architecture/8.5-Kubernetes-Orchestration-v1.0.06-07.md) | Kubernetes Orchestration | Pods, services, operators, Helm charts |
| [8.6](8-Software-Architecture/8.6-Multi-Tenancy-v1.0.06-07.md) | Multi-Tenancy Patterns | Shared database, shared schema, isolated tenancy |
| [8.7](8-Software-Architecture/8.7-Cell-Based-Architecture-v1.0.06-07.md) | Cell-Based Architecture | Ringpop, sharding cells, blast radius limits |
| [8.8](8-Software-Architecture/8.8-Feature-Flags-v1.0.06-07.md) | Feature Flags | Progressive delivery, kill switches, A/B testing |

---

## Section 9: Platform DevOps

**Platform Engineering & Security**

Modern platform engineering practices and zero-trust security.

| Module | Title | Description |
|--------|-------|-------------|
| [9.1](9-Platform-DevOps/9.1-Platform-Lifecycles-v1.0.06-07.md) | Platform Lifecycles | CI/CD, infrastructure as code, platform APIs |
| [9.2](9-Platform-DevOps/9.2-Zero-Trust-Security-v1.0.06-07.md) | Zero-Trust Security | Identity, cryptography, network isolation, service mesh |

---

## Section 10: Production Engineering

**Operational Excellence & Resiliency**

Production-grade observability, reliability, and chaos engineering.

| Module | Title | Description |
|--------|-------|-------------|
| [10.1](10-Production-Engineering/10.1-Observability-Telemetry-v1.0.06-07.md) | Observability & Telemetry | Metrics, logs, traces, golden signals |
| [10.2](10-Production-Engineering/10.2-SRE-Principles-v1.0.06-07.md) | SRE Principles | Error budgets, SLIs/SLOs, toil reduction |
| [10.3](10-Production-Engineering/10.3-Resiliency-Chaos-v1.0.06-07.md) | Resiliency & Chaos | Circuit breakers, chaos engineering, fault injection |

---

## Section 11: AI Systems

**Planet-Scale AI, Agents & LLMOps**

Modern AI infrastructure from ingestion to inference at scale.

| Module | Title | Description |
|--------|-------|-------------|
| [11.1](11-AI-Systems/11.1-Ingestion-Vector-Search-v1.0.06-07.md) | Ingestion & Vector Search | RAG pipelines, embedding models, similarity search |
| [11.2](11-AI-Systems/11.2-Distributed-Inference-KV-Cache-v1.0.06-07.md) | Distributed Inference & KV Cache | Model serving, cache optimization, inference scheduling |
| [11.3](11-AI-Systems/11.3-Model-Fine-Tuning-Safety-v1.0.06-07.md) | Model Fine-Tuning & Safety | Parameter-efficient tuning, RLHF, guardrails |
| [11.4](11-AI-Systems/11.4-AI-Agent-Architectures-v1.0.06-07.md) | AI Agent Architectures | ReAct, plan-and-execute, tool use, memory systems |
| [11.5](11-AI-Systems/11.5-Model-Context-Protocol-v1.0.06-07.md) | Model Context Protocol | MCP architecture, context management, tool protocols |
| [11.6](11-AI-Systems/11.6-Agent-to-Agent-Protocol-v1.0.06-07.md) | Agent-to-Agent Protocol | A2A communication, inter-agent discovery |
| [11.7](11-AI-Systems/11.7-LangChain-Ecosystem-v1.0.06-07.md) | LangChain Ecosystem | LangChain, LangGraph, LangSmith, orchestration frameworks |
| [11.8](11-AI-Systems/11.8-Context-Engineering-v1.0.06-07.md) | Context Engineering | Prompt optimization, context windows, token budgeting |
| [11.9](11-AI-Systems/11.9-AI-Skills-LLM-Gateways-v1.0.06-07.md) | AI Skills & LLM Gateways | Tool calling, function composition, LLM routing |
| [11.10](11-AI-Systems/11.10-MLOps-LLMOps-v1.0.06-07.md) | MLOps/LLMOps Lifecycle | Model versioning, deployment, monitoring |

---

## Section 12: Multi-Region

**Global Scale Architecture**

Multi-region deployment strategies and global failure handling.

| Module | Title | Description |
|--------|-------|-------------|
| [12.1](12-Multi-Region/12.1-Global-Traffic-Management-v1.0.06-07.md) | Global Traffic Management | DNS routing, Anycast, CDN failover |
| [12.2](12-Multi-Region/12.2-Multi-Region-Data-Strategy-v1.0.06-07.md) | Multi-Region Data Strategy | Global databases, data sovereignty, replication lag |
| [12.3](12-Multi-Region/12.3-Global-Catastrophic-Failure-v1.0.06-07.md) | Global Catastrophic Failure | Disaster recovery, multi-region failover, chaos at scale |

---

## Section 13: Design Trade-offs

**Archetype Trade-off Patterns**

Classic architectural trade-offs and decision frameworks.

| Module | Title | Description |
|--------|-------|-------------|
| [13.1](13-Design-Tradeoffs/13.1-Tradeoffs-v1.0.06-07.md) | Trade-off Patterns | Consistency vs availability, latency vs throughput, cost vs performance |

---

## Section 14: Case Studies

**Real-World System Design Analysis**

Deep-dive case studies applying the curriculum framework.

| Module | Title | Description |
|--------|-------|-------------|
| [14.1](14-Case-Studies/14.1-Classic-Interview-Problems-v1.0.06-07.md) | Classic Interview Problems | URL shortener, rate limiter, cache design |
| [14.2](14-Case-Studies/14.2-Communication-Collaboration-v1.0.06-07.md) | Communication & Collaboration | Slack, Teams, real-time messaging |
| [14.3](14-Case-Studies/14.3-Media-Content-v1.0.06-07.md) | Media & Content | YouTube, Netflix, content delivery |
| [14.4](14-Case-Studies/14.4-Marketplace-Commerce-v1.0.06-07.md) | Marketplace & Commerce | Amazon, Shopify, payment systems |
| [14.5](14-Case-Studies/14.5-Social-Discovery-v1.0.06-07.md) | Social & Discovery | Twitter, Instagram, feed distribution |
| [14.6](14-Case-Studies/14.6-Infrastructure-Platform-v1.0.06-07.md) | Infrastructure & Platform | AWS, Kubernetes, platform APIs |
| [14.7](14-Case-Studies/14.7-FinTech-Deep-Dive-v1.0.06-07.md) | FinTech Deep Dive | Payment systems, exchanges, regulatory compliance |
| [14.8](14-Case-Studies/14.8-Industry-Architectures-v1.0.06-07.md) | Industry Architectures | Uber, Airbnb, Stripe, architectural deep-dives |

---

## Quick Reference Guides

| Guide | Description |
|-------|-------------|
| [Master Guide](enhanced-system-design-master-guide.md) | Complete syllabus and discussion framework |

---

## Usage

### Reading Order

For systematic study, follow the numbered sections sequentially. Each section builds on concepts from previous sections:

1. Start with Section 1 (Foundations) to understand core primitives
2. Proceed to Sections 2-4 for data plane foundations
3. Sections 5-7 cover distributed systems patterns
4. Sections 8-9 address application architecture
5. Sections 10-13 cover operational concerns and modern AI
6. Section 14 applies all concepts to real systems

### Each Module Follows

Each technical module follows this deep-dive structure:

1. **What It Is** — Concrete definition with real-world anchor
2. **Core Dimensions** — Deep dive with Cause→Approach→Trade-off analysis
3. **Cross-Connections** — Links to related concepts across modules
4. **Failure Modes** — Production edge cases and mitigation patterns
5. **Interview Questions** — Graded questions (⭐ mid-level, ⭐⭐ senior, ⭐⭐⭐ staff/principal)

---

## License

**Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)**

You are free to:
- ✅ Share — Copy and redistribute this material in any medium or format
- ✅ Adapt — Remix, transform, and build upon this work

**Under the following terms:**
- **Attribution** — You must give appropriate credit to Dennis Jacob, provide a link to the license, and indicate if changes were made
- **NonCommercial** — You may not use this material for commercial purposes without explicit permission

**Recommended attribution format:**
```
Source: Master System Design Curriculum by Dennis Jacob
https://github.com/dennisjacob/systemdesign
License: CC BY-NC 4.0
```

---

## Contributing

This is a personal curriculum repository. For questions or discussions:
- Open an issue on GitHub
- Contact the maintainer

---

© 2026 Dennis Jacob. All original content. Licensed under CC BY-NC 4.0.