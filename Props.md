# 🔗 Props, Immutability, and One-Way Data Flow

**Tags:** #React #Props #DataFlow #Immutability #Components  
**Links:** [[Components]] [[State]] [[Component Composition]] [[JSX]]

---

## ⚡ Core Idea
**Props** (short for *properties*) are how data flows **from parent to child components** in React.  
They are **read-only**, ensuring a **one-way data flow** and keeping components predictable and isolated.

---

## 💡 Key Points
- Props are **inputs** to components.  
- Passed like **HTML attributes**, received as **function parameters**.  
- **Immutable**: a child component **cannot modify** its props.  
- Data only flows **downward (one-way)** from parent → child.

---

## 🔍 Example
**Parent Component:**
```jsx
function App() {
  return <Welcome name="Tasos" />;
}
```

**Child Component:**
```jsx
function Welcome({ name }) {
  return <h1>Hello, {name}!</h1>;
}
```

Here, `name="Tasos"` is passed **down** to the `Welcome` component as a prop.

---

## 🚫 Why Immutability Matters
- Prevents **unexpected side effects**.  
- Makes React’s **re-render logic** efficient.  
- Enables **pure components** — outputs depend only on inputs (props).  

---

## 🧩 Visualization
```
Parent (App) → Child (Welcome) → UI
```
Data moves in one direction only — **top to bottom**.

---

## 🧠 Summary
Props enforce React’s key principle:  
> “Data flows down, actions flow up — predictable, immutable, and easy to reason about.”
