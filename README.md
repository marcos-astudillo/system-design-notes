# system-design-notes

A curated set of system design documents and reusable templates focused on **backend engineering** and **system architecture**.  
Each design is written with an interview-ready structure: requirements → architecture → APIs → data model → scaling → trade-offs.

> Target audience: backend engineers (mid-level) preparing for system design interviews or building architecture muscle memory.

![Stars](https://img.shields.io/github/stars/marcos-astudillo/system-design-notes?style=flat)
![License](https://img.shields.io/github/license/marcos-astudillo/system-design-notes?style=flat)
![Last Commit](https://img.shields.io/github/last-commit/marcos-astudillo/system-design-notes)
![Repo Size](https://img.shields.io/github/repo-size/marcos-astudillo/system-design-notes)
![Architecture](https://img.shields.io/badge/architecture-distributed%20systems-blue?style=flat)
![System Design](https://img.shields.io/badge/system%20design-interview%20ready-brightgreen?style=flat)

---

## Goals

This repository is part of a personal learning project focused on improving system design and backend architecture skills.

The goals of this project are:

- Practice designing real-world distributed systems
- Document architecture decisions clearly
- Understand scalability trade-offs
- Implement selected systems as working services
- Build a public portfolio of backend engineering work

---

## Table of Contents

- [How to Use This Repo](#how-to-use-this-repo)
- [Repository Structure](#repository-structure)
- [System Design Roadmap (10 Systems)](#system-design-roadmap-10-systems)
- [Methodology](#methodology)
- [Design Template](#design-template)
- [Guides](#guides)
- [Designs](#designs)
- [License](#license)

---

## How to Use This Repo

1. Start with the **template** in [`templates/design-template.md`](templates/design-template.md).
2. Read designs in the [`designs/`](designs/) folder in any order, or follow the roadmap below.
3. For each design, focus on:
   - Requirements and assumptions (the “contract”)
   - High-level architecture (the “shape”)
   - APIs and data model (the “interfaces”)
   - Scaling strategy and bottlenecks (the “real world”)
   - Trade-offs and improvements (the “engineering judgement”)

If you're preparing for interviews, practice doing a 30–45 minute walkthrough per design:
- 5 min: requirements + assumptions
- 10 min: architecture
- 10 min: API + data model
- 10 min: scaling + bottlenecks
- 5–10 min: trade-offs + improvements

---

## Repository Structure

```
system-design-notes/
  README.md
  LICENSE
  templates/
    design-template.md
  guides/
    how-to-write.md
  roadmap/
    weekly-roadmap.md
  designs/
    url-shortener.md
    rate-limiter.md
    chat-system.md
    api-gateway.md
    search-autocomplete.md
    notification-system.md
    file-storage.md
    recommendation-system.md
    analytics-pipeline.md
    job-queue.md
```

---

## System Design Roadmap (10 Systems)

1. **URL Shortener** — write path, id generation, caching, analytics basics
2. **Rate Limiter (Token Bucket + Redis)** — distributed coordination, correctness vs throughput
3. **Chat System (WebSockets + fanout)** — real-time, presence, ordering, delivery semantics
4. **API Gateway** — auth, routing, quotas, observability, edge concerns
5. **Search Autocomplete** — prefix index, latency, ranking, hot keys
6. **Notification System** — multi-channel delivery, retries, idempotency, templates
7. **File Storage System** — upload, metadata, blob storage, CDN, consistency
8. **Recommendation System** — candidate generation, ranking, feature store, feedback loops
9. **Analytics Pipeline** — ingestion, ETL, batch vs streaming, data lake/warehouse
10. **Distributed Job Queue** — scheduling, retries, backoff, dead-letter, exactly-once-ish

A weekly plan to produce these designs lives in [`roadmap/weekly-roadmap.md`](roadmap/weekly-roadmap.md).

---

## Methodology

All documents follow the same structure to keep the reasoning consistent and scannable:

1. **Problem statement**: define boundaries (what we are/aren’t building).
2. **Functional requirements**: what the system must do.
3. **Non-functional requirements**: SLOs, scale, reliability, security, and cost constraints.
4. **Assumptions**: explicit numbers, patterns, and constraints that shape the design.
5. **High-level architecture**: components and data flow (with Mermaid diagrams).
6. **API design**: external contracts and important internal interfaces.
7. **Data model**: schema, indexes, partitioning keys, and retention.
8. **Scaling strategy**: how we grow without breaking latency/cost.
9. **Bottlenecks**: the likely failure points.
10. **Trade-offs**: alternatives and why we choose one approach.
11. **Possible improvements**: what you'd do next with more time or more scale.

This format is close to how experienced engineers communicate designs: **constraints → shape → interfaces → operations**.

---

## Design Template

- [`templates/design-template.md`](templates/design-template.md)

---

## Guides

- [`guides/how-to-write.md`](guides/how-to-write.md) — how to write high-signal system design docs
- [`roadmap/weekly-roadmap.md`](roadmap/weekly-roadmap.md) — 10-week plan (1 design/week)

---

## Designs

- [URL Shortener](designs/url-shortener.md)
- [Rate Limiter (Token Bucket + Redis)](designs/rate-limiter.md)
- [Chat System (WebSockets + fanout)](designs/chat-system.md)
- [API Gateway](designs/api-gateway.md)
- [Search Autocomplete](designs/search-autocomplete.md)
- [Notification System](designs/notification-system.md)
- [File Storage System](designs/file-storage.md)
- [Recommendation System](designs/recommendation-system.md)
- [Analytics Pipeline](designs/analytics-pipeline.md)
- [Distributed Job Queue](designs/job-queue.md)

---

## Implementations

The following system designs also have practical implementations demonstrating how these architectures can be built in real systems.

| System | Design | Implementation |
|------|------|------|
| URL Shortener | [Design](designs/url-shortener.md) | Coming soon |
| Rate Limiter | [Design](designs/rate-limiter.md) | Coming soon |
| Chat System | [Design](designs/chat-system.md) | Coming soon |
| API Gateway | [Design](designs/api-gateway.md) | Coming soon |
| Search Autocomplete | [Design](designs/search-autocomplete.md) | Coming soon |
| Notification System | [Design](designs/notification-system.md) | Coming soon |
| File Storage System | [Design](designs/file-storage.md) | Coming soon |
| Recommendation System | [Design](designs/recommendation-system.md) | Coming soon |
| Analytics Pipeline | [Design](designs/analytics-pipeline.md) | Coming soon |
| Distributed Job Queue | [Design](designs/job-queue.md) | Coming soon |

---

## License

MIT — see [`LICENSE`](LICENSE).

> Note: Replace `<USER>` in the badges with your GitHub username.
