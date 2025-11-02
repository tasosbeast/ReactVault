# What Does the Front-End Do?

## Primary Responsibility
- Keep the **user interface (UI)** synchronized with the available application **state**.
- Reflect data changes immediately so the interface feels responsive and reliable.

## How React Helps
1. Components receive data via props or state.
2. When the data changes, React triggers a new render pass.
3. The updated virtual DOM is diffed against the previous render.
4. Only the changed UI elements are patched in the browser, ensuring the view stays in sync.

## Best Practices
- Treat state as the single source of truth for what the UI should display.
- Avoid duplicating data across multiple state containers unless necessary.
- Model UI updates declaratively—describe the final result, and let React handle the DOM work.

## Related Topics
- [[UI]] — The visual representation users interact with.
- [[State]] — Data that drives component behavior and rendering.
- [[Render]] — The process React uses to produce UI from state and props.
