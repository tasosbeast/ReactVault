# ⚖️ State vs Props

**Tags:** #React #State #Props #DataFlow #Components  
**Links:** [[State]] [[Props]] [[Components]]

---

## ⚡ Core Idea
**State** and **props** are both sources of data for a React component — but they serve **different purposes**.  
State is **internal** and **mutable**, while props are **external** and **immutable**.

---

## 💡 Key Differences

| Aspect | State | Props |
|--------|--------|--------|
| **Ownership** | Managed *inside* the component | Received *from parent* |
| **Mutability** | Can change over time (`setState`) | Read-only |
| **Purpose** | Store dynamic data | Pass data or callbacks to children |
| **Trigger Re-render** | Yes, when updated | Yes, when changed |
| **Direction** | Internal (component logic) | External (parent → child) |

---

## 🔍 Example
```jsx
function Counter({ step }) {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={() => setCount(count + step)}>+{step}</button>
    </div>
  );
}

// Parent
<App>
  <Counter step={5} />
</App>
```

- `step` → **prop**, controlled by parent.  
- `count` → **state**, controlled by the component itself.

---

## 🧩 Visualization
```
Parent (props ↓) → Child (state inside) → Renders UI
```
Props flow **downward**, state lives **inside**.

---

## 🧠 Summary
State vs Props:  
> “Props are external inputs. State is internal memory. Together, they keep React components reactive and predictable.”
