# ADR 0001: Monolith vs. Microservices

## Status
Accepted

## Context
The team must choose between a modular monolith and microservices for the initial platform architecture.

## Decision
Start with a modular monolith for faster iteration and simpler deployment. Plan clear module boundaries to enable future migration to microservices.

## Consequences
- Faster MVP delivery
- Lower operational complexity early
- Easier to refactor into services as scale demands

## References
- [MonolithFirst by Martin Fowler](https://martinfowler.com/bliki/MonolithFirst.html)
