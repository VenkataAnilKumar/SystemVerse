# Mock Interview: Design a URL Shortener

## Prompt
Design a scalable URL shortening service like bit.ly. Discuss API design, storage, scaling, and edge cases.

## Model Answer Outline
- RESTful API: POST /shorten, GET /{code}
- Store mappings in NoSQL (e.g., DynamoDB)
- Use base62 encoding for short codes
- Caching for popular links
- Handle collisions, abuse, and analytics

## Evaluation Rubric
- Clarity of requirements
- API and data model design
- Scalability and fault tolerance
- Security and abuse prevention
- Communication and trade-off analysis

## References
- [System Design Primer: URL Shortener](https://github.com/donnemartin/system-design-primer#design-a-url-shortener)
