# 🧭 Fundamentals of State Management

**Tags:** #React #StateManagement #Hooks #Architecture #DataFlow  
**Links:** [[State|What is State in React]] [[State|More Thoughts About State and Guidelines]] [[State-vs-Props|State vs Props]] [[What-is-Thinking-in-React|What is Thinking in React]] [[Derived State]] [[useReducer]]

---

## ⚡ Core Idea
State management is the **art of controlling how data changes over time** and how those changes affect the UI.  
Good state management ensures your app stays **predictable**, **maintainable**, and **efficient** — even as it grows.

---

## 💡 Core Principles

1. **Single Source of Truth**
   - Keep the “real” state in one place.  
   - Derive everything else (like filtered lists or computed values) from that source.

2. **Unidirectional Data Flow**
   - Data always moves **down** from parent → child (via props).  
   - Changes move **up** via callbacks.

3. **Local vs Global State**
   - **Local:** Belongs to a single component (e.g. a form input).  
   - **Global:** Shared across multiple components (e.g. theme, user, cart).

4. **State Lifting**
   - Move state **up** the component tree when several components need it.  
   - Avoid duplication — centralize shared state.

5. **Immutability**
   - Always create new objects or arrays instead of mutating old ones.  
   - Keeps re-renders and diffing predictable.

---

## 🔍 Example
```jsx
function App() {
  const [items, setItems] = useState(["🍎", "🍌", "🍇"]);
  const [filter, setFilter] = useState("");

  const visibleItems = items.filter((item) =>
    item.toLowerCase().includes(filter.toLowerCase())
  );

  return (
    <div>
      <SearchBar filter={filter} onFilterChange={setFilter} />
      <ItemList items={visibleItems} />
    </div>
  );
}
```
Here, `App` holds the **shared state** — `SearchBar` and `ItemList` just receive props.

---

## 🧩 Visualization
```
Single Source of Truth (App)
↓ Props Down
↑ Events Up
→ Derived State for UI Rendering
```

---

## 🧠 Summary
State management is about:  
> “Keeping your data organized, your updates predictable, and your UI in sync with reality.”
