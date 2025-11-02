# Why React Re-renders on State Changes

## Core Idea
- React components produce UI output based on their **state** and **props**.
- When either of these inputs change, React recalculates the component's output so the UI mirrors the current data.

## Re-render Lifecycle
1. A state update is scheduled via `setState`, `useState`, or another state management API.
2. React marks the component (and potentially its descendants) as needing to render again.
3. The component function/class render method runs to produce a new virtual DOM tree.
4. React diffs the new tree against the previous one and applies the minimal DOM updates.

## Practical Implications
- Keep state updates focused and localized to avoid unnecessary work.
- Derive expensive computations outside the render path or memoize them.
- Ensure state represents the single source of truth to maintain predictable UI behavior.

## Related Concepts
- [[State]] — Data owned by a component.
- [[Virtual DOM]] — Tree structure used for diffing updates.
- [[Re-render]] — The act of recalculating a component's output.
