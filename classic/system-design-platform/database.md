
# Database Design

Database design is foundational to system performance, scalability, and correctness. This section covers practical strategies, examples, and checklists for robust data management.

## Storage Choices

### 1. Relational Databases (PostgreSQL/MySQL)
- Best for structured data, strong consistency, and complex queries (e.g., users, catalog, enrollments, payments).
- Use normalization, foreign keys, and ACID transactions.
- **Checklist:**
	- [ ] All tables have primary keys
	- [ ] Foreign keys enforce referential integrity
	- [ ] Use transactions for multi-step updates
	- [ ] See [PostgreSQL Official Docs](https://www.postgresql.org/docs/)

### 2. NoSQL Databases (MongoDB/Elastic)
- Use for unstructured or semi-structured data, high write throughput, or flexible schemas (e.g., forum posts, analytics, search indexes).
- Document, key-value, and column-family stores for different needs.
- **Checklist:**
	- [ ] Choose the right NoSQL model for your use case
	- [ ] Index frequently queried fields
	- [ ] Plan for schema evolution
	- [ ] See [MongoDB Data Modeling](https://www.mongodb.com/docs/manual/core/data-modeling-introduction/)

---

## Data Modeling

### Example Entities
- **User:** id, name, email, password_hash, role, created_at
- **CatalogItem:** id, title, description, price, published, created_at
- **Enrollment:** id, user_id, catalog_id, status, enrolled_at
- **Progress:** id, user_id, catalog_id, lesson_id, completed_at

### Best Practices
- Use normalization for transactional data, denormalization for analytics.
- Store audit logs for critical changes.
- Use UUIDs for distributed systems.

### Checklist
- [ ] All sensitive data is encrypted at rest
- [ ] Indexes exist for all frequent queries
- [ ] Data retention and archival policies are defined
- [ ] Sharding/partitioning strategy is documented

---

## Caching

### 1. Redis
- Use for session tokens, frequently accessed catalog data, and user progress.
- Implement cache invalidation strategies (TTL, write-through, cache-aside).
- **Checklist:**
	- [ ] All cache keys have TTLs
	- [ ] Cache hit/miss metrics are monitored
	- [ ] See [Redis Caching Patterns](https://redis.io/docs/management/cache/)

### 2. CDN
- Serve static assets (images, videos, docs) from a CDN for low latency and offload from origin servers.

---

## Actionable Checklist
- [ ] Choose the right storage engine for each use case
- [ ] Document all data models and relationships
- [ ] Regularly review and optimize indexes
- [ ] Monitor query performance and storage growth

---

## References
- [PostgreSQL Official Docs](https://www.postgresql.org/docs/)
- [MongoDB Data Modeling Best Practices](https://www.mongodb.com/docs/manual/core/data-modeling-introduction/)
- [Redis Caching Strategies](https://redis.io/docs/management/cache/)
- [Awesome Scalability](https://github.com/binhnguyennus/awesome-scalability)
