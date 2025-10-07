
# Functional & Non-Functional Requirements

This section covers the essential requirements for any robust system, with practical examples and actionable checklists.

## Functional Requirements
Functional requirements define what the system should do. They are derived from user needs, business goals, and domain analysis. For a modern education or learning platform, typical functional requirements include:

### 1. User Authentication
- Secure sign up, login, and password reset.
- Use OAuth2, JWT, and strong password hashing (e.g., bcrypt).
- Multi-factor authentication (MFA) for sensitive actions.
- **Checklist:**
	- [ ] All authentication endpoints use HTTPS
	- [ ] Passwords are never stored in plain text
	- [ ] Rate limiting on login attempts
	- [ ] MFA available for users
	- [ ] Session expiration and refresh tokens implemented
	- [ ] See [OWASP Authentication Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)

### 2. User Profile Management
- Update personal info, preferences, and privacy settings.
- Avatar upload, notification preferences, and account deletion.

### 3. Course/Catalog Management
- CRUD operations for courses, search, filtering, and recommendations.
- Faceted search, full-text indexing, and tagging.
- **Checklist:**
	- [ ] Search supports filtering and sorting
	- [ ] Course metadata is normalized
	- [ ] Recommendations are personalized
	- [ ] See [Elasticsearch: The Definitive Guide](https://www.elastic.co/guide/en/elasticsearch/guide/current/index.html)

### 4. Enrollment
- Support both free and paid enrollments, with transactional integrity.
- Waitlists, prerequisites, and batch enrollments.

### 5. Progress Tracking
- Track user progress at module/lesson granularity.
- Store as event logs or summary tables for analytics.

### 6. Quizzes and Assignments
- Auto/manual grading, plagiarism detection, and feedback loops.
- Timed quizzes, randomization, and question banks.
- **Reference:** [Designing Data-Intensive Applications, Ch. 10]

### 7. Discussion Forums
- Threaded discussions per module, moderation tools, and notifications.
- Upvotes, reporting, and sticky threads.

### 8. Payments and Subscriptions
- Integrate with PCI-compliant providers (Stripe, PayPal).
- Handle refunds, chargebacks, and recurring billing.

### 9. Admin Panel
- Role-based access for managing users, content, and analytics.
- Audit logs, bulk actions, and analytics dashboards.

---

## Non-Functional Requirements
Non-functional requirements (NFRs) define system qualities and constraints. They are critical for real-world success and often drive architectural decisions.

### 1. High Availability
- Design for 99.9%+ uptime.
- Use redundancy, failover, and health checks.
- **Checklist:**
	- [ ] Load balancers in front of all critical services
	- [ ] Health checks for all service endpoints
	- [ ] Multi-AZ or multi-region deployment
	- [ ] See [Google SRE Book, Ch. 21]

### 2. Low Latency
- Aim for sub-200ms response times for user actions.
- Use caching, CDNs, and async processing.

### 3. Fault Tolerance
- Graceful degradation, retries, and circuit breakers.
- Chaos engineering to test resilience.
- **Reference:** [Release It! by Michael Nygard]

### 4. Security
- Follow OWASP Top 10, encrypt sensitive data, and use RBAC.
- Regular security audits and penetration testing.
- **Checklist:**
	- [ ] All sensitive data encrypted at rest and in transit
	- [ ] RBAC enforced for all admin actions
	- [ ] Regular vulnerability scans
	- [ ] See [OWASP Top 10](https://owasp.org/www-project-top-ten/)

### 5. Monitoring & Observability
- Collect metrics, logs, and traces.
- Use tools like Prometheus, Grafana, and ELK stack.
- Alerting on SLO/SLA breaches.

### 6. Scalability
- Design to handle 10x user spikes.
- Use horizontal scaling, stateless services, and partitioning.

### 7. Maintainability
- Modular, testable codebase.
- Use CI/CD, code reviews, and automated testing.

---
For more, see [The System Design Primer](https://github.com/donnemartin/system-design-primer) and [Awesome Scalability](https://github.com/binhnguyennus/awesome-scalability).
