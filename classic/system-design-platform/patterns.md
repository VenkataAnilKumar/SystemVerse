# Design Patterns & Principles

Design patterns are reusable solutions to common problems in software architecture. Principles guide the structure and evolution of robust systems.

## Core Patterns
- **Singleton:** Ensure a class has only one instance (e.g., DB connection pool, config loader). Use with care to avoid hidden dependencies. [GoF Design Patterns]
- **Factory:** Encapsulate object creation logic (e.g., user/session/token creation). Promotes loose coupling.
- **Observer:** Notify dependent components of state changes (e.g., notification system for emails/SMS). Enables event-driven architectures.
- **Strategy:** Encapsulate interchangeable algorithms (e.g., payment gateway selection, grading logic).
- **Repository:** Abstract data access, enabling decoupling between business logic and persistence.

## Architectural Principles
- **SOLID:** Five principles for maintainable, extensible code (Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, Dependency Inversion). [SOLID Principles](https://en.wikipedia.org/wiki/SOLID)
- **DRY (Don’t Repeat Yourself):** Avoid code duplication.
- **KISS (Keep It Simple, Stupid):** Prefer simplicity over complexity.
- **YAGNI (You Aren’t Gonna Need It):** Don’t implement features until necessary.

## References
- [Design Patterns: Elements of Reusable Object-Oriented Software](https://en.wikipedia.org/wiki/Design_Patterns) (GoF)
- [Refactoring Guru: Patterns](https://refactoring.guru/design-patterns)
- [Awesome Scalability](https://github.com/binhnguyennus/awesome-scalability)
