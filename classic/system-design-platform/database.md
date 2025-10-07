# Database Design

Database design is foundational to system performance, scalability, and correctness. Choose the right data model and storage engine based on your access patterns and consistency needs.

## Storage Choices
- **Relational DB (PostgreSQL/MySQL):** Best for structured data, strong consistency, and complex queries (e.g., users, catalog, enrollments, payments). Use normalization, foreign keys, and ACID transactions. [See: PostgreSQL Official Docs](https://www.postgresql.org/docs/)
- **NoSQL (MongoDB/Elastic):** Use for unstructured or semi-structured data, high write throughput, or flexible schemas (e.g., forum posts, analytics, search indexes). [See: MongoDB Data Modeling](https://www.mongodb.com/docs/manual/core/data-modeling-introduction/)

## Data Modeling
- **User:** id, name, email, password_hash, role, created_at
- **CatalogItem:** id, title, description, price, published, created_at
- **Enrollment:** id, user_id, catalog_id, status, enrolled_at
- **Progress:** id, user_id, catalog_id, lesson_id, completed_at

Design for:
- **Referential integrity:** Use foreign keys or application-level checks.
- **Indexing:** Add indexes for frequent queries (e.g., user_id, catalog_id).
- **Sharding/partitioning:** For very large tables, consider horizontal partitioning.

## Caching
- **Redis:** Use for session tokens, frequently accessed catalog data, and user progress. [Redis Caching Patterns](https://redis.io/docs/management/cache/)
- **CDN:** Serve static assets (images, videos, docs) from a CDN for low latency and offload from origin servers.

## References
- [PostgreSQL Official Docs](https://www.postgresql.org/docs/)
- [MongoDB Data Modeling Best Practices](https://www.mongodb.com/docs/manual/core/data-modeling-introduction/)
- [Redis Caching Strategies](https://redis.io/docs/management/cache/)
- [Awesome Scalability](https://github.com/binhnguyennus/awesome-scalability)
