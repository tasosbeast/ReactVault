# Data Equals State in React

## Core Principle
- The visual output of a React application is a direct projection of the component **state**.
- If you know the current state, you can predict exactly what the **UI** will render.

## Render Flow
1. State is updated through React APIs such as `setState` or hooks like `useState`.
2. React triggers a **re-render** of the affected component tree.
3. The render result (React elements) is compared with the previous virtual DOM snapshot.
4. Only the changed pieces of the real DOM are updated so the UI stays in sync with the state.

## Why It Matters
- Encourages a single source of truth for UI data, making components easier to reason about.
- Reduces UI bugs caused by manual DOM manipulation or duplicated data sources.
- Sets the foundation for predictable testing and debugging workflows.

## Related Concepts
- [[State]] — The data a component owns and reacts to.
- [[Re-render]] — The process triggered when state changes.
- [[UI]] — The interface that reflects the current state values.
