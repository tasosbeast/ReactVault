# 🧮 Derived State

**Tags:** #React #State #DerivedState #BestPractices #Performance  
**Links:** [[Fundamentals-of-State-Management|Fundamentals of State Management]] [[State|What is State in React]] [[State|More Thoughts About State and Guidelines]] [[useMemo]] [[State-vs-Props|State vs Props]]

---

## ⚡ Core Idea
**Derived state** is data that can be **computed from existing state or props** — it doesn’t need to be stored separately.  
By avoiding redundant state, you prevent bugs, simplify your logic, and keep your components more efficient.

---

## 💡 When to Derive Instead of Store

| Situation | Example | Why Not Store It? |
|------------|----------|------------------|
| You can calculate it from existing data | `const count = items.length;` | It auto-updates when items change |
| It’s a filtered or sorted version of state | `const filtered = todos.filter(t => t.done);` | No need to sync two states |
| It’s a visual flag | `const isEmpty = list.length === 0;` | It depends on `list`, not independent |

---

## 🔍 Example
```jsx
function TodoList({ todos, showDone }) {
  const visibleTodos = showDone
    ? todos.filter((t) => t.done)
    : todos.filter((t) => !t.done);

  return (
    <ul>
      {visibleTodos.map((todo) => (
        <li key={todo.id}>{todo.text}</li>
      ))}
    </ul>
  );
}
```
`visibleTodos` is **derived** from `todos` and `showDone` — no extra state needed.

---

## ⚠️ When *Not* to Derive
- If computation is **expensive** (e.g. large dataset filtering), memoize it with `useMemo`.  
- If it’s **user-controlled data**, store it in state instead.

---

## 🧩 Visualization
```
Base State (truth) → Derived Values → Rendered UI
```

The fewer states you store, the fewer sync issues you’ll face.

---

## 🧠 Summary
Derived state helps you keep logic clean:  
> “Don’t store what you can calculate — derive it instead.”
