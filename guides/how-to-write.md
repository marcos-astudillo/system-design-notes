# How to Write High-Signal System Design Documents

This guide focuses on writing system design docs that are **easy to review**, **easy to discuss**, and **useful for interviews**.

---

## What reviewers look for

- **Clear problem boundaries** (no scope creep)
- **Explicit assumptions** (numbers drive architecture)
- **Interfaces first** (APIs and contracts)
- **Operational maturity** (deploy, observe, debug, recover)
- **Trade-offs** (you know alternatives and consequences)

---

## Suggested writing approach

1. **Write requirements and assumptions first**
   - You cannot design effectively without constraints.
   - Add order-of-magnitude numbers (QPS, payload sizes, retention).
2. **Draw a high-level diagram**
   - Keep it simple: 6–10 boxes max.
3. **Define the external API**
   - Inputs/outputs, auth, errors, pagination, idempotency.
4. **Define the data model**
   - Primary keys, indexes, partition keys, TTL, cardinalities.
5. **Write the scaling and reliability plan**
   - Caches, queues, shards, replicas, multi-region.
6. **Call out bottlenecks & trade-offs**
   - “Where will it hurt first?” and “What did we sacrifice?”
7. **List improvements**
   - Show forward thinking without rewriting the system.

---

## What to include (and what to avoid)

### Include
- Mermaid diagrams (architecture + 1 sequence diagram when it helps)
- SLO targets (latency/availability) even if rough
- Operational topics: retries, timeouts, DLQ, alerting, dashboards
- Data lifecycle: retention, GDPR deletion, backups, disaster recovery

### Avoid
- Vague statements like “use Kafka for scale” without stating **why**
- Too many vendor-specific details unless the design is explicitly vendor-bound
- Unrealistic “perfect” guarantees (e.g., global strong consistency for everything)

---

## Practical checklist

- [ ] Can someone summarize the system in 30 seconds after reading the first section?
- [ ] Are assumptions numeric and consistent across the doc?
- [ ] Do APIs include idempotency strategy where needed?
- [ ] Does the data model show keys + indexes and how queries are served?
- [ ] Do you explain failure modes (retries, partial failures, timeouts)?
- [ ] Do you state bottlenecks and how you would mitigate them?
- [ ] Do you list trade-offs with at least 2 alternatives?

---

## Naming and tone

Write as if this doc will be reviewed by your team:
- Use short paragraphs
- Prefer bullets for lists
- Use consistent headers
- Keep diagrams readable in GitHub
