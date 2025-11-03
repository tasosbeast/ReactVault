# ⚛️ What is React?

**Tags:** #React #Library #Frontend #Theory  
**Links:** [[Why-Do-Front-End-Frameworks-Exist|Why Do Front-End Frameworks Exist]] [[Components]] [[JSX]] [[State|State and UI Sync]]

---

## ⚡ Core Idea
React is a **declarative**, **component-based**, **[[state]]-driven** JavaScript **library** for building user interfaces.  
It updates the UI automatically when data ([[state]]) changes.

---

## 💡 Key Points
- React focuses only on the **View layer** (UI) — not a full framework.  
- Built by **Facebook (2011)** and open-sourced in **2013**.  
- Uses a **virtual DOM** for efficient rendering.  
- Everything is built using **[[components]]** (small, reusable UI pieces).  
- Written using **[[JSX]]**, a syntax that mixes HTML + JS.  

---

## 🧩 Visualization
```
[[STATE]] → React → Virtual DOM → Real DOM → UI
```
React compares changes between renders and updates only what’s necessary.

---

## 🔍 Example (Basic Component)
```jsx
function Welcome() {
  return <h1>Hello, world!</h1>;
}
```

React will render this component and keep it updated automatically.

---

## 🧠 Summary
React is:  
> “A JavaScript library for building dynamic, declarative, component-based user interfaces.”
