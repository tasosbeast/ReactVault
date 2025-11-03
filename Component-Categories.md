# 🧩 Component Categories

**Tags:** #React #Components #Architecture #StateManagement #UI  
**Links:** [[Component Composition]] [[Components]] [[State-vs-Props|State vs Props]] [[Rendering-Lists|Rendering Lists]]

---

## ⚡ Core Idea
Not all components serve the same purpose.  
In React, we often group components into **categories** based on what they do — separating **logic** from **presentation**.  
This makes apps more modular, reusable, and easier to reason about.

---

## 💡 Common Categories

### 1️⃣ Presentational (UI) Components
- Focus purely on **how things look**.  
- Receive data via **props**, display it, but **don’t manage state**.  
- Usually written as **small functional components**.  

```jsx
function UserCard({ name, avatar }) {
  return (
    <div className="card">
      <img src={avatar} alt={name} />
      <p>{name}</p>
    </div>
  );
}
```

🧩 Example: Buttons, Cards, Headers, Layout Wrappers.

---

### 2️⃣ Container (Logic) Components
- Handle **data fetching**, **state**, and **logic**.  
- Pass data down to presentational components as props.  
- Decide *what* to render, not *how* it looks.

```jsx
function UserContainer() {
  const [users, setUsers] = useState([]);

  useEffect(() => {
    fetch("/api/users")
      .then((res) => res.json())
      .then(setUsers);
  }, []);

  return users.map((u) => <UserCard key={u.id} {...u} />);
}
```

🧠 Example: Data providers, layout controllers, parent components.

---

### 3️⃣ Hybrid Components
Some components naturally do both — especially at small scale.  
That’s fine, as long as you stay consistent and refactor when they grow.

---

## 🧩 Visualization
```
Container (logic, data)
   ↓ props
Presentational (UI)
```

This keeps your app clean and predictable as it scales.

---

## 🧠 Summary
React doesn’t enforce component types — but *thinking in categories* helps you design better:  
> “Separate how it looks from how it works.”
