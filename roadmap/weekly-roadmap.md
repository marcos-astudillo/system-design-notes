# Weekly Roadmap (1 Design per Week)

A 10-week plan to complete the repo. Each week ends with a **review + improvement pass**.

> Suggestion: timebox each design to ~4–6 hours total. Aim for clarity over completeness.

---

## Week 1 — URL Shortener
- Draft requirements + assumptions
- Decide id generation approach
- Add caching plan and analytics hooks
- Add 1 sequence diagram (shorten + redirect)

## Week 2 — Rate Limiter (Token Bucket + Redis)
- Define correctness requirements (burst, fairness, consistency)
- Design Lua-based atomic operations in Redis
- Consider local cache + Redis fallback
- Add failure modes and mitigation

## Week 3 — Chat System (WebSockets + fanout)
- Cover connection lifecycle, presence, delivery semantics
- Add fanout approach (push vs pull)
- Discuss ordering and storage strategy
- Add scaling for large rooms

## Week 4 — API Gateway
- Route, authN/authZ, quotas, caching, transforms
- Add observability section (logs, traces, metrics)
- Include plugin architecture as an improvement

## Week 5 — Search Autocomplete
- Model prefix index options (Trie vs inverted index)
- Add hot key mitigation and ranking strategy
- Add cache/TTL and offline build process

## Week 6 — Notification System
- Multi-channel delivery (email/SMS/push)
- Idempotency and template rendering
- Retry with backoff + DLQ
- Include user preferences and quiet hours

## Week 7 — File Storage System
- Multipart upload, metadata, virus scanning
- Durable blob storage + CDN
- Lifecycle policies and deletion
- Signed URLs and access control

## Week 8 — Recommendation System
- Candidate generation + ranking
- Feature store and training loop
- Feedback and A/B testing
- Cold start strategies

## Week 9 — Analytics Pipeline
- Ingestion, stream vs batch
- Data lake/warehouse layers
- Data quality and schema evolution
- Cost management and retention

## Week 10 — Distributed Job Queue
- Scheduling, retries, leases, visibility timeout
- Exactly-once-ish patterns
- Rate limiting / backpressure
- Worker autoscaling

---

## Review rubric (use every week)
- Does the architecture match the assumptions?
- Are there at least 3 explicit trade-offs?
- Can a reader find the API + data model quickly?
- Is the system operable (alerts, dashboards, runbook notes)?
