# How React Handles the DOM vs. Vanilla JavaScript

## Vanilla JavaScript Workflow
- You manually query DOM nodes and imperatively update attributes, text, and event listeners.
- Complex UIs require bookkeeping to avoid inconsistent state between the DOM and in-memory data.

## React Workflow
1. You describe the desired UI using **JSX** (a declarative structure).
2. React builds a **virtual DOM** representation of that UI.
3. During reconciliation, React diff-checks the virtual DOM against the previous snapshot.
4. Only the minimal DOM operations needed to reach the new UI are executed.

## Benefits of React's Approach
- **Predictability:** UI is a function of state and props rather than manual DOM mutations.
- **Maintainability:** Components encapsulate UI logic, reducing duplicated imperative code.
- **Performance:** Batched updates and diffing prevent unnecessary DOM work.

## Key Terms
- [[DOM]] — The browser's object model for rendered elements.
- [[JSX]] — Syntax extension for describing UI structure in JavaScript.
- [[Virtual DOM]] — Lightweight tree React uses to compute efficient updates.
