# 📋 Rendering Lists

**Tags:** #React #Lists #Rendering #Keys #Performance  
**Links:** [[Component Composition]] [[Props]] [[State]] 

---

## ⚡ Core Idea
React can render lists of elements dynamically by **mapping over arrays**.  
Each rendered item needs a **unique key** to help React efficiently update, add, or remove elements in the UI.

---

## 💡 Key Concepts
- Use `Array.map()` to turn data into JSX.  
- Each item must have a **unique `key` prop**.  
- Keys help React identify which elements changed, improving performance and avoiding re-renders of unchanged items.

---

## 🔍 Example — Rendering an Array
```jsx
function UserList({ users }) {
  return (
    <ul>
      {users.map((user) => (
        <li key={user.id}>{user.name}</li>
      ))}
    </ul>
  );
}

function App() {
  const users = [
    { id: 1, name: "Tasos" },
    { id: 2, name: "Valia" },
  ];
  return <UserList users={users} />;
}
```

---

## ⚠️ Keys: Why They Matter
Without unique keys, React struggles to track which list items changed.  
That can cause UI glitches — for example, incorrect reordering or lost input state.

**Never use array indexes** as keys when elements can be reordered or removed.  
Use stable IDs instead.

---

## 🧩 Visualization
```
Data Array → map() → List of JSX Elements (each with key)
```

React uses the `key` to compare new and old lists efficiently.

---

## 🧠 Summary
Rendering lists in React:  
> “Map your data to JSX — and always give each element a stable identity with a key.”
