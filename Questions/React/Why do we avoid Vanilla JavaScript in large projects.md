# Why Avoid Vanilla JavaScript in Large Projects?

## Core Challenges
- Imperative DOM manipulation scales poorly—tracking updates across many files becomes brittle.
- Shared state and cross-component communication are difficult without formal patterns.
- Testing and refactoring are harder when UI logic is spread across ad-hoc scripts.

## How Frameworks Help
- **Structure:** Enforce component-based organization that encapsulates markup, style, and behavior.
- **State Management:** Provide predictable data flow (e.g., React state, context, or external stores).
- **Tooling:** Offer build pipelines, devtools, and ecosystem support for routing, forms, and more.

## When Vanilla JS Still Works
- Small widgets or pages with limited interactivity.
- Prototyping experiments where long-term maintainability is not a priority.

## Related Concepts
- [[State]] — The evolving data your UI depends on.
- [[Bugs]] — Errors that multiply when logic is duplicated or unsynchronized.
- [[Component]] — A reusable building block encouraged by frameworks like React.
